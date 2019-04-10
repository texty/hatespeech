<template>
  <div id="app">

<main>
<div id="left-parent">
  <h1>Прихльники Порошенко</h1>
      <svg width="100%" height="100%" viewBox="0 0 400 1000">
          <g transform="translate(-50, -50)">
            <text :class="[item.ua_ === true ? 'ua text' : 'ru text']" v-for="item in leftData" :x="item.x" :y="item.y"  
            :style="[currentDate === item.check ? {'font-size': '20px'} : {'font-size': '0'}]"> #{{ item.key}} </text>
                   
          </g>
        </svg>

        

</div>

<div>
<h1 id="date">{{ dateToShow }}</h1>    

<p> <span style="color:red;">Неукраїнський твіттер (російський, суржик, визначала лібою - сhrome's language identification library (cld)  тощо)</span>, <span style="color:blue;">україномовний</span></p>
<p>Активні напади на Порошенко почались в травні 2014 року в російськомовному твітері</p>
<p>"Дурналисты", "журнализды" - активно використується в російськомовному твітері (десь з 2009 року), часто по відношення до рос. ЗМІ, а також до американських ЗМІ. Не додавала поки рос. написання - "Журнализды", "Дурнализды", "Медиабляди" - дуже багато з них не стосується України, але в російськомовий твіттері іх ДУЖЕ багато</p>
<p>Під час Майдану ці слова використовуються по відношенню до рос. ЗМІ, в укр. контексті</p>
<p>Наприкінці 2017 року починається рвань.</p>
</div>


<div id="right-parent">
   <h1>Противники Порошенко</h1>
 <svg width="100%" height="100%" viewBox="0 0 400 1000">
          <g transform="translate(-50, -50)">
            <text :class="[item.ua_ === true ? 'ua text' : 'ru text']" v-for="item in rightData" :x="item.x" :y="item.y"  
            :style="[currentDate === item.check ? {'font-size': '20px'} : {'font-size': '0'}]"> #{{ item.key }} </text>
                   
          </g>
        </svg> 

</div>

</main>

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
import data2 from "./assets/data/data2.json";

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
     leftData: function() {
     data1.map(function(val) {
        val.x = 100+Math.floor(Math.random() * 200);
        val.y = 100+Math.floor(Math.random() * window.innerHeight);
        var theDate = new Date(val.date);
        val.check = theDate.getTime(); 
      })
    return(data1);
    },
    rightData: function() {
      data2.map(function(val) {
        val.x = 100+Math.floor(Math.random() * 200);
        val.y = 100+Math.floor(Math.random() * window.innerHeight);        
        var theDate = new Date(val.date);
        val.check = theDate.getTime(); 
      })
    return(data2);
    },

    dates: function(){
      var that = this;  
      var leftDates = that.leftData.map(function(x) {
            return new Date(x["date"]);
      });
      var rightDates = that.rightData.map(function(x) {
            return new Date(x["date"]);
      })
      var uniquedates = [];
      leftDates.forEach(function(d){
      if(!uniquedates.includes(d.getTime())){  
          uniquedates.push(d.getTime())
        }
      })
      rightDates.forEach(function(d){
      if(!uniquedates.includes(d.getTime())){  
          uniquedates.push(d.getTime())
        }
      })
      uniquedates.sort(function(a,b){ return new Date(a) - new Date(b); });
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
