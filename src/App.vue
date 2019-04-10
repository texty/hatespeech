<template>
  <div id="app">


<div id="left-parent">
      <svg width="100%" height="100%" viewBox="0 0 400 1000">
          <g transform="translate(-50, -50)">
            <text class="text" v-for="item in mydata" :x="item.x" :y="item.y"  
            :style="[currentDate === item.check ? {'font-size': '20px'} : {'font-size': '0'}]"> #{{ item.key }} </text>
                   
          </g>
        </svg>

        <h1 id="date">{{ dateToShow }}</h1>      

</div>




  <!--   <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view /> -->
  </div>
</template>

<script>
import * as d3 from "d3";
import data1 from "./assets/data/data1.json";

var formatDate = d3.timeFormat("%d-%m-%Y")


export default {
  data() {
    return {
      n: 0
    }
  },
  watch: {  
   
   
  },

  mounted: function() { 
    this.runMe();


   },

  methods: {  
    drawPoints: function() { 
      var that = this;      
        
          setTimeout(function(){          
          if(that.n < that.dates.length-1){
              that.n = that.n + 1   
          } else {
            return false
          }
          
            
          }, 500)
                     
     },
     
     runMe: function() {
       var that = this; 
        setInterval(function(){
          that.drawPoints()
        }, 500)

     }
    
  },
  computed: {
     mydata: function() {
     data1.map(function(val) {
        val.x = 100+Math.floor(Math.random() * 200);
        val.y = 100+Math.floor(Math.random() * window.innerHeight);
        val.color = "orange"
        var theDate = new Date(val.date);
        val.check = theDate.getTime(); 
      })
    return(data1);
    },

    dates: function(){
      var that = this;  
      var alldates = that.mydata.map(function(x) {
            return new Date(x["date"]);
      });
      var uniquedates = [];
      alldates.forEach(function(d){

      if(!uniquedates.includes(d.getTime())){  
          console.log(d.getTime())   
          uniquedates.push(d.getTime())
        }
      })
      uniquedates.sort(function(a,b){
          return new Date(a) - new Date(b);
      });
      return(uniquedates)    
    },

    latest: function() {
      var that = this;  
      var latest = new Date(Math.max.apply(null, that.dates));     
      return(latest)
    },
    currentDate: function() {
        var that = this;  
        var current = that.dates[that.n];
        console.log(current) 
        return(current)
    },

    dateToShow: function() {
      var that = this;  
      var dateTo = formatDate(that.currentDate)      
      return(dateTo)
    },
 
    
  }
  }


</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Roboto");
@import 'assets/style.scss';


</style>
