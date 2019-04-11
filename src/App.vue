<template>
  <div id="app">

<main>
<div id="left-parent">
  <h4>Прихльники Порошенко</h4>
  <p class="date">{{ dateToShow }}</p>    

<!--       <svg width="100%" height="100%" viewBox="0 0 400 1000">
          <g transform="translate(-50, 0)">
            <text :class="[item.ua_ === true ? 'ua text' : 'ru text']" v-for="item in leftData" :x="item.x" :y="item.y"  
            :style="[currentDate === item.check ? {'font-size': '20px'} : {'font-size': '0'}]"> #{{ item.key}} </text>
                   
          </g>
        </svg> -->

        

</div>

<div id="content">
  <div id="inner">
  <button @click="stop = !stop">Стоп</button>
<!-- 
  <p> <span style="color:red;">Неукраїнський твіттер (російський, суржик, визначала лібою - сhrome's language identification library (cld)  тощо)</span>, <span style="color:blue;">україномовний</span></p>
  <p>Активні напади на Порошенко почались в травні 2014 року в російськомовному твітері</p>
  <p>"Дурналисты", "журнализды" - активно використується в російськомовному твітері (десь з 2009 року), часто по відношення до рос. ЗМІ, а також до американських ЗМІ. Не додавала поки рос. написання - "Журнализды", "Дурнализды", "Медиабляди" - дуже багато з них не стосується України, але в російськомовий твіттері іх ДУЖЕ багато</p>
  <p>Під час Майдану ці слова використовуються по відношенню до рос. ЗМІ, в укр. контексті</p>
  <p>Наприкінці 2017 року починається рвань.</p>
 -->

  <h1>Зрадофіли vs порохоботи</h1>
  <h3>Хроніки ворожнечі на політичному грунті. </h3>

  <div id="bricksContainer">
  
    <div id="bricks-for">
      <p>
        <span>зрадофіли</span>
        <span>зрадойоби</span>
        <span>корисні ідіоти</span>
        <span>хробацьке</span>
        <span>медіабляді</span>
        <span>грантожери</span>
        <span>радіосволота</span>
        <span>недорогенькі</span>
        <span>журналізди</span>
        <span>дурналісти</span>
        <span>медіаповії</span>
        <span>перемога</span>
      </p>
    </div>

    <div id="bricks-against">
      <p>
        <span>порохоботи</span>
        <span>петяботи</span>
        <span>шоколадник</span>
        <span>поросенко</span>
        <span>порохопідари</span>
        <span>вальцман</span>
        <span>порохоботи-підари</span>
        <span>інфопиздота</span>
        <span>жидипоновому</span>
        <span>сліпотрасти</span>
        <span>зрада</span>
      </p>
    </div>
  </div>


  <h2>Почалось з "Поросенко"</h2>
  <p>  26 січня 20014 року - "Песец какой-то, чтобы я пошел бить кого-то ради олигарха, типа Поросенко. Они что, футбольные клубы вместе с фанатами покупают?" - це був перший твіт, де Порошенка назвали "Поросенко".  Локація його автора (Максим Бейлис (https://twitter.com/maxbeylis)) в акаунті не вказана, але більшість його постів стосується Росії і Карахстана. </p>
  <p>Вибори в Україні також зацікавили користувача https://twitter.com/Baba_Jagodka, в якої локацією взаний Мінськ Біларусь, але в ії твіттер скоріше нагадує чат-бота, ніж людину. Зареєструвалась за два тижня до зазначеного твіта</p>
  <p>  В лютому 2014 року "Поросенко" трохи хвилював юзерів з російськомовного твітера - Росії, Білорусі, а також Севастополя.</p>
  <p>  В цей же час в російськомовному твітері зʼявляється образливе слово "шоколданик", в українському твітері, воно не прижилось</p>
  <p>  Поодинокі "поросенко" і "шоколадник" то там то тут до травня 2015 року.</p>
  <p>  25 травня - в цей день 2014 року ми обирали в першому турі Петра Порошенка - 19 твітів з "порсенко", усі російською мовою. Після виборів "поросенко" прижився в російськомовному твітері серйозно і надовго.</p>
  
  <div class="chart">
    <p><b>#поросенко</b><span class="against">ua-твітер</span><span class="support">ru-твітер</span></p>
      <svg width="100%" height="100%" viewBox="0 0 600 200">
        <g transform="translate(30, -40)" >
          <path id="porosenko_ua_path" class="linechartpath" :d='porosenko_ua_path' stroke="orange" stroke-width='2px' fill="none" />
          <path id="porosenko_ru_path" class="linechartpath" :d='porosenko_ru_path' stroke="silver" stroke-width='1px' fill="none" />     
          <g v-axisY="[0, porosenko_ua.maxCount]" transform="translate(0, 0)" style="font-size:10px; fill:grey"></g>
          <g v-axisX="[porosenko_ua.minDate, porosenko_ua.maxDate]" transform="translate(0, 200)" style="font-size:10px; fill:grey"></g>

          <line :x1="scale.x(new Date('2014-05-25'))" :x2="scale.x(new Date('2014-05-25'))" :y1="scale.y(0)" :y2="scale.y(200)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
          <line :x1="scale.x(new Date('2017-05-17'))" :x2="scale.x(new Date('2017-05-17'))" :y1="scale.y(0)" :y2="scale.y(200)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
          <line :x1="scale.x(new Date('2019-01-06'))" :x2="scale.x(new Date('2019-01-06'))" :y1="scale.y(0)" :y2="scale.y(200)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
       
          <text :y="-scale.x(new Date('2014-06-15'))" x="50" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">вибори</text>
          <text :y="-scale.x(new Date('2017-05-30'))" x="50" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">безвіз</text>
          <text :y="-scale.x(new Date('2019-01-20'))" x="50" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">томос</text>
        </g>
   </svg>
   </div>

   <h2>В протилежному таборі</h2>
  <p>  26 січня 20014 року - "Песец какой-то, чтобы я пошел бить кого-то ради олигарха, типа Поросенко. Они что, футбольные клубы вместе с фанатами покупают?" - це був перший твіт, де Порошенка назвали "Поросенко".  Локація його автора (Максим Бейлис (https://twitter.com/maxbeylis)) в акаунті не вказана, але більшість його постів стосується Росії і Карахстана. </p>
  <p>Вибори в Україні також зацікавили користувача https://twitter.com/Baba_Jagodka, в якої локацією взаний Мінськ Біларусь, але в ії твіттер скоріше нагадує чат-бота, ніж людину. Зареєструвалась за два тижня до зазначеного твіта</p>
  <p>  В лютому 2014 року "Поросенко" трохи хвилював юзерів з російськомовного твітера - Росії, Білорусі, а також Севастополя.</p>
  <p>  В цей же час в російськомовному твітері зʼявляється образливе слово "шоколданик", в українському твітері, воно не прижилось</p>
  <p>  Поодинокі "поросенко" і "шоколадник" то там то тут до травня 2015 року.</p>
  <p>  25 травня - в цей день 2014 року ми обирали в першому турі Петра Порошенка - 19 твітів з "порсенко", усі російською мовою. Після виборів "поросенко" прижився в російськомовному твітері серйозно і надовго.</p>

  
  






</div>

</div>


<div id="right-parent">
   <h4>Противники Порошенко</h4>
   <p class="date">{{ dateToShow }}</p>    

<!--  <svg width="100%" height="100%" viewBox="0 0 400 1000">
          <g transform="translate(-50, 0)">
            <text :class="[item.ua_ === true ? 'ua text' : 'ru text']" v-for="item in rightData" :x="item.x" :y="item.y"  
            :style="[currentDate === item.check ? {'font-size': '20px'} : {'font-size': '0'}]"> #{{ item.key }} </text>
                   
          </g>
        </svg> 
 -->
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
import porosenko from "./assets/data/porosenko.json";


/* var formatDate = d3.timeFormat("%d-%m-%Y")
var parseDate = d3.timeFormat("%Y-%m-%d"); */

export default {
  data() {
    return {
      turn: 0.5,
      formatDate: d3.timeFormat("%d-%m-%Y"),
      parseDate:d3.timeParse("%Y-%m-%d"),
      n: 0,
      stop: false,
      width: 600,
      height: 200,
      margin: {
        top: 30,
        bottom: 50,
        left: 30,
        right: 30,
        
      },
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
          if(that.n < that.dates.length-1 & that.stop === false){
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
    porosenko_ua: function(){
     var that = this; 
     var data = porosenko.filter(function(d){ return d.ua_ === true;  })       
     var maxCount = d3.max(data, function(d) { return +d.count } );  

     var dates = data.map(function(x) { return new Date(x.week) })
     
     data.forEach(function(row){        
       row.week = that.parseDate(row.week)
     }) 
     
     var unique_dates = [];
     dates.forEach(function(row){
       if(!unique_dates.includes(row.getTime())){
         unique_dates.push(row.getTime())
       }
     })
     var minDate = new Date(Math.min.apply(null, unique_dates));   
     var maxDate = new Date(Math.max.apply(null, unique_dates));   

     return  { data, maxCount, minDate, maxDate }
    },
    porosenko_ru: function(){
     var that = this; 
     var data = porosenko.filter(function(d){ return d.ua_ === false;  })       
     var maxCount = d3.max(data, function(d) { return +d.count } );  

     var dates = data.map(function(x) { return new Date(x.week) })
     
     data.forEach(function(row){        
       row.week = that.parseDate(row.week)
     }) 
     
     var unique_dates = [];
     dates.forEach(function(row){
       if(!unique_dates.includes(row.getTime())){
         unique_dates.push(row.getTime())
       }
     })
     var minDate = new Date(Math.min.apply(null, unique_dates));   
     var maxDate = new Date(Math.max.apply(null, unique_dates));   

     return  { data, maxCount, minDate, maxDate }
    },

    





    //срач-чарт
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
        return(current)
    },

    dateToShow: function() {
      var that = this;  
      var dateTo = that.formatDate(that.currentDate)      
      return(dateTo)
    },
    scale() {
      var that = this; 
      var y = d3.scaleLinear()
        .range([that.height, 0])
        .domain([0, 240])
          
      var x = d3.scaleTime()
        .range([0, that.width])
        .domain([new Date("2013-12-01"), new Date("2020-01-01")])
        return { x, y };
    },
    //функції відмальовки лайнчартів
    d3LinePath: function() {
      var that = this;     
      const path = d3.line()
        .x(d => that.scale.x(d.week))
        .y(d => that.scale.y(+d.count));
      return (path)
    },
    porosenko_ua_path: function () {   
      var that = this;        
      var newLine = that.d3LinePath(that.porosenko_ua.data) 
      return(newLine)
    },   
    porosenko_ru_path: function () {   
      var that = this;        
      var newLine = that.d3LinePath(that.porosenko_ru.data) 
      return(newLine)
    },  
  },
    directives: {    
    axisY(el, binding, vnode) {            
      const that = this;     

/*       vnode.context.scale.y.domain(binding.value)
 */      
      d3.select(el).call(d3.axisLeft(vnode.context.scale.y)
       
      );
    },
    axisX(el, binding, vnode) {            
      const that = this;     
      
/*       vnode.context.scale.x.domain(binding.value)
 */
      d3.select(el).call(d3.axisBottom(vnode.context.scale.x)
      );
    }
  }
  }





</script>

<style lang="scss">
@import 'assets/style.scss';


</style>
