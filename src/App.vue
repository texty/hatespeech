<template>
  <div id="app">

<main>
<div id="left-parent">
 <!--  <h4>Прихльники Порошенко</h4> -->
<!--   <p class="date">{{ dateToShow }}</p>    
 -->
<!--       <svg width="100%" height="100%" viewBox="0 0 400 1000">
          <g transform="translate(-50, 0)">
            <text :class="[item.ua_ === true ? 'ua text' : 'ru text']" v-for="item in leftData" :x="item.x" :y="item.y"  
            :style="[currentDate === item.check ? {'font-size': '20px'} : {'font-size': '0'}]"> #{{ item.key}} </text>
                   
          </g>
        </svg> -->

        

</div>

<div id="content">
  <div id="inner">
  <!-- <button @click="stop = !stop">Стоп</button> -->
<!-- 
  <p> <span style="color:red;">Неукраїнський твіттер (російський, суржик, визначала лібою - сhrome's language identification library (cld)  тощо)</span>, <span style="color:blue;">україномовний</span></p>
  <p>Активні напади на Порошенко почались в травні 2014 року в російськомовному твітері</p>
  <p>"Дурналисты", "журнализды" - активно використується в російськомовному твітері (десь з 2009 року), часто по відношення до рос. ЗМІ, а також до американських ЗМІ. Не додавала поки рос. написання - "Журнализды", "Дурнализды", "Медиабляди" - дуже багато з них не стосується України, але в російськомовий твіттері іх ДУЖЕ багато</p>
  <p>Під час Майдану ці слова використовуються по відношенню до рос. ЗМІ, в укр. контексті</p>
  <p>Наприкінці 2017 року починається рвань.</p>
 -->

  <h1>Зрадофіли, порохоботи, медіабляді. 
</h1>
  <h3>Хроніки розпалення ворожнечі в українському твітері. 
 </h3>

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


<!--   <div class="chart">
    <h3><b>#поросенко</b><span class="against">ua-твітер</span><span class="support">ru-твітер</span></h3>
      <svg width="100%" height="100%" viewBox="0 0 600 200">
        <g transform="translate(50, -40)" >
          <path id="porosenko_ua_path" class="linechartpath" :d='porosenko_ua_path' stroke="orange" stroke-width='2px' fill="none" />
          <path id="porosenko_ru_path" class="linechartpath" :d='porosenko_ru_path' stroke="silver" stroke-width='1px' fill="none" />     
          <g v-axisY="[0, porosenko_data.maxCount]" transform="translate(0, 0)" style="font-size:10px; fill:grey"></g>
          <g v-axisX="" transform="translate(0, 200)" style="font-size:10px; fill:grey"></g>

          <line :x1="scale.x(new Date('2014-05-25'))" :x2="scale.x(new Date('2014-05-25'))" :y1="scale.y(0)" :y2="scale.y(200)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
          <line :x1="scale.x(new Date('2017-05-17'))" :x2="scale.x(new Date('2017-05-17'))" :y1="scale.y(0)" :y2="scale.y(200)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
          <line :x1="scale.x(new Date('2019-01-06'))" :x2="scale.x(new Date('2019-01-06'))" :y1="scale.y(0)" :y2="scale.y(200)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
       
          <text :y="-scale.x(new Date('2014-06-15'))" x="40" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">вибори</text>
          <text :y="-scale.x(new Date('2017-05-30'))" x="40" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">безвіз</text>
          <text :y="-scale.x(new Date('2019-01-20'))" x="40" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">томос</text>
        </g>
   </svg>
   </div> -->

   <h2>Журналістів “Інтера” частіше називали медіаблядями, а журналістів 1+1 медіхвойдами.
</h2>

<p>Мова ворожнечі до представників ЗМІ - раніше ніж у нас зʼявилась в Росії. Там ще з 2008-2010 рр. журналістів почали називати лайливими похідними від їхньої професії</p>
<p>“Дурналисты” та “Журнашлюхи” використовувалось по відношенню до будь-яких фейлів у медіа. Очевидні джинса, відкриті або приховані маніпуляції в медіа, неперевірині факти або просто у ЗМІ висловлена думка, яку юзер не поділяє: все це є приводами для лайки. Юзери з прокремлівськими поглядами таким чином характеризували зокрема європейську та американську пресу. Юзери, що не підтримували офіційну інформаціну лінію  - по відношенню до “рупорів Кремля”.
</p>


 <img class="responsive" src="./assets/img/dyrnalisty.png" />
 <img class="responsive" src="./assets/img/zhyrnashluhi.png" />

<p>Під час Майдану в українському твітері або в українському контектсі зʼявляється лайка “журнашлюхи” : <br><br>
  <span style=background-color:orange>січень 2014 </span><br><br>
  <span style=background-color:lightgrey>“Смотрю новости на Интере, желаю журнашлюхам гореть в аду”</span><br><br>
   <span style=background-color:orange>лютий 2014</span><br><br>
  <span style=background-color:lightgrey>“Происходящее сейчас в Киеве великолепно высветило потроха росиянских сми….”</span><br><br>
  <span style=background-color:lightgrey>"Тимошенко підвелася на ноги з інвалідного візка" кажуть журнашлюхи. А хіба Вам казали що у Тимошенко віднялись ноги?</span><br><br>

  <span style=background-color:orange>березень 2014</span><br><br>
  <span style=background-color:lightgrey>“Вкрючите Россия 24 Там Америкос журношлюх нам подводит что мы Виноваты во всём что происходит на Украине”</span><br><br>
  <span style=background-color:orange>березень 2014</span><br><br>
  <span style=background-color:lightgrey>“путинских журнашлюх пора расстреливать”</span><br><br>
</p>

<p>Однак активізуються лайки на адресу журналістів  після розслідування “Слідство.інфо” про офшори Порошенка. Громадське звинуватили в тому, що розслідування є маніпулятивним через помилку в перекладі. Детальніше тут. З протилежного боку лунала думка, що кампанію проти журналістів запустили так звані “порохоботи” (тобто проплачені прихильники Порошенка), аби нівелювати цінність розслідування. В цей час здебільшого на адресу Громадського, але не тільки, сипляться числені образливі епітети: “дурналісти”, “хробацьке”, “журнашлюхи”, “жопагнапа” тощо. 
</p>
 <img class="responsive" src="./assets/img/hrobatske.png" />
  <img class="responsive" src="./assets/img/zhopagnapa.png" />

 

<p>Літо 2016 року  - скандал щодо співпраці телеканалу Інтер з ЛНР/ДНР. <br><br>
<span style=background-color:orange>серпень 2016 р.</span><br><br>
<span style=background-color:lightgrey>“Стало зрозуміло чому медіабляді так цькували Миротворець. Їм заважали налагоджувати "сатруднічєство".”</span><br><br>

<span style=background-color:lightgrey>“твит одобрен "днр"? #медиабляди #журнашлюхи”</span><br><br>

<span style=background-color:lightgrey>Обнародованные документы - приговор для каждой #медиабляди ! Marina Daniluk-Ermolaeva точна и беспощадна на все 100</span><br><br>

<span style=background-color:lightgrey>“Бочкала з Інтеру. Медіаблядей Інтера попалив Миротворець на співпраці з лугандонськими макаками.”</span><br><br>

</p>

 <img class="responsive" src="./assets/img/mediablyadi.png" />


 
 <p>Наступним етапом є березень 2018 року - після прес- конференції Петра Порошенка, яка відбулась 28 лютого. Тоді Детектор медіа підсумував, що висвітлення прес-конференції  в ЗМІ було здебільшого однобічно позитивним чи однобічно негативним. На захід було акредетовано понад 200 представників ЗМІ, було чимало незручних питань президентов, зокрема про відпочинок на Мальдівах. Після прес-конференції Петра Порошенка звинуватили у сексизмі через його зверненння до однієї із журналісток “дорогенька”. Це стало початком  флешмобу “я тобі не дорогенька”, а  інформаціний простір поповнився ще однією лайкою “недорогенькі”, з натяком на дешевість і продажність журналістів і медіа. Медіахвойди, медіповії  - також активізуються в твітері в цей період.</p>

  <img class="responsive" src="./assets/img/nedorogenki.png" />


<p>Брудна неофіційна передвиборча кампанія, численна джинса активізує образливі хештеги наприкінці 2018 - початку 2019 рр. Медіа знову, хтось заслужено, а хтось ні отримують порцію лайна. У січні 2019 чимало претензій і матюків присвячується телеканалу 1+1, зокрема тснua, через тендеційну позицію і піар Зеленського. За подекуди проросійську позиції достається bbcua.</p>

<img class="responsive" src="./assets/img/mediahvoqdy.png" />
  <img class="responsive" src="./assets/img/mediapovii.png" />

<p>А от “пропагандони”, що в російськомовному, що в україномовному твітері здебільшого використовуються на адресу російської пропаганд машини.</p>
 <img class="responsive" src="./assets/img/propagandony.png" />






<h2>Грантожери та корисні ідіоти
</h2>

<p>Ображати громадські організації, які працюють на рахунок донорських коштів - також більш актуально для російсьмовного твітера. 
“Грантоеды” в Росії - дуже погані люди, які працюють на ворогів, підтриваючи державу.</p>
<p>Цікаво, що до 2012 року це слово вилазить рідко і в ньому фігурують різні пострадянські країни. Але, починаючи з 2012 році контекст  уходить до Росії, де тоді ухвалюють закон «Про некомерційні організації” більш відомий як закон про іноземних агентів.</p>
<p>В україномовному твітері лайка активізується після того, як речниця Луценка назвала істерикою грантожерів заяви Холодницького і НАБУ. Далі тему грантожерів здебільшого розвивають прихильники Порошенка, вважаючи, що саме через велику кількість антикорупційних грантів, журналісти приплетають президента до усіх можливих корупційних скандалів і створюють картину суцільної зради, ігноруючи усі позитивні досягнення.</p>
 <img class="responsive" src="./assets/img/grantozhery.png" />



 <img class="responsive" src="./assets/img/idiots.png" />

 <h2>Мову ворожнечі до Порошенка та його прихильників нам намагались навʼязати, але ми сказали “ніт” і придумали власну
</h2>
 
 <p>Відразу після президентських виборів 2014 року в російськомовному твітері Порошенка починають образливо називати  “Поросенко” і “Шоколадник”.  В перший місяць після виборів лайка “Поросенко” досягла 600 твіттів. Наприкінці 2014 р. - початку 2015 р. активно розкурчується “Шоколадник” в контексті Липецької фабрики “Рошен”. Але обидва слова в україномовному твітері так і не прижились. 
</p>

 <img class="responsive" src="./assets/img/porosenko.png" />


<p>Натомість десь вже наприкінці 2014-початку 2015 рр. зʼявляється помітне інформаційне протистояння між “порохоботами” “зрадофілами”.
</p>

<p>Зустрічаються і більш радикальні варіанти - “зрадойоби” і “порохопідари”, але набагато рідше.
</p>

<p>Лінії обої слів мають схожу траекторію. Піки активності припадають на:<br><br>
<span style=background-color:orange>березень 2017 р. </span> -  суд на тодішнім головою ДФС Романом Насировим,<br><br>
<span style=background-color:orange>жовтень 2017 р.</span> - завява Порошенка “зрадофілам хоч тризуб над кремлем постав - скажуть, що криво”,<br><br>
<span style=background-color:orange>грудень 2017 р. </span>- так звана “кава на Майдані” - флешмоб прихильників Порошенка на противагу прихильників Саакашвілі, <br><br>
<span style=background-color:orange>березень 2018 р.</span>  - після прес-конференції Порошенка, <br><br>
а також <span style=background-color:orange>грудень 2018 р.</span> - активізація неофіційної передвиборчої кампанії, активне обговорення надання Україні Томосу.

</p>

 <img class="responsive" src="./assets/img/porohoboty.png" />
  <img class="responsive" src="./assets/img/zradofily.png" />
 <img class="responsive" src="./assets/img/zradoyoby.png" />


<h2>Вже зрозуміло, що порохоботами все не скінчиться, адже напередодні першого туру зʼявились нові лайки, які характеризують прихильність до нового президента України Володимира Зеленського - "зебіли", "зеботи", "з"едебіли" тощо</h2>

 <img class="responsive" src="./assets/img/benija.png" />

 <p>Що ж такого сталось, що за 5 рокік українське суспільство стало таким поляризованим? Звісно, ми не маємо даних про усе суспільство, але нараз соціальні мережі є репрезентативним відзеркаленням того, що відбувається</p> 

 <p>Звісно, ми не відкриємо Америки, якщо скажемо, що має місце також штучне розпалення ворожнечі в мережі. І те, що ми образливо називаємо одне одного зрадофілами, порохоботами або зелеботами не значить, що паралелньно з цим не працюють технології, завдянням яких є максимально помоножити цю ворожнечу</p>

<p>В нашоу вибірку для цього матеріалу потрапило лише 300 тис. твітів, але навіть серед них є мережі ботів. Так 99 юзерів, які активно використовували мову ворожнечі і написали понад 1300 твітів 99 - зареєстровано в один день 27 серпня 2014 р.</p>





   <!-- <div class="chart">
    <h3><b>#порохоботи</b><span class="against">ua-твітер</span><span class="support">ru-твітер</span></h3>
      <svg width="100%" height="100%" viewBox="0 0 600 200">
        <g transform="translate(50, -40)" >
          <path id="porohoboty_ua_path" class="linechartpath" :d='porohoboty_ua_path' stroke="orange" stroke-width='2px' fill="none" />
          <path id="porohoboty_ru_path" class="linechartpath" :d='porohoboty_ru_path' stroke="silver" stroke-width='1px' fill="none" />     
          <g v-axisY="[0, porohoboty_data.maxCount]" transform="translate(0, 0)" style="font-size:10px; fill:grey"></g>
          <g v-axisX="" transform="translate(0, 200)" style="font-size:10px; fill:grey"></g>

          <line :x1="scale.x(new Date('2014-05-25'))" :x2="scale.x(new Date('2014-05-25'))" :y1="scale.y(0)" :y2="scale.y(porohoboty_data.maxCount)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
          <line :x1="scale.x(new Date('2017-05-17'))" :x2="scale.x(new Date('2017-05-17'))" :y1="scale.y(0)" :y2="scale.y(porohoboty_data.maxCount)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
          <line :x1="scale.x(new Date('2019-01-06'))" :x2="scale.x(new Date('2019-01-06'))" :y1="scale.y(0)" :y2="scale.y(porohoboty_data.maxCount)" style="stroke-width:0.5px; stroke:grey; stroke-dasharray: 3,3; "/>
       
          <text :y="-scale.x(new Date('2014-06-15'))" x="40" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">вибори</text>
          <text :y="-scale.x(new Date('2017-05-30'))" x="40" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">безвіз</text>
          <text :y="-scale.x(new Date('2019-01-20'))" x="40" transform="translate(0, 0), rotate(90)" style="font-size:11px; fill:grey">томос</text>
        </g>
   </svg>
   </div>
 -->


  






</div>

</div>


<div id="right-parent">
  <!--  <h4>Противники Порошенко</h4>
   <p class="date">{{ dateToShow }}</p>     -->

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
import porohoboty from "./assets/data/porohoboty.json";
import zradoyoby from "./assets/data/zradoyoby.json";




/* var formatDate = d3.timeFormat("%d-%m-%Y")
var parseDate = d3.timeFormat("%Y-%m-%d"); */

export default {
  data() {
    return {
      porosenko_ua_path: '',
      porosenko_ru_path: '',
      porohoboty_ua_path: '',
      porohoboty_ru_path: '',
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
        left: 50,
        right: 30,
        
      },
    }
  },
  watch: {  
   
   
  },

  mounted: function() { 
    /* this.runMe();
    this.porosenko_ua_path = this.d3LinePath(this.porosenko_data.dataUA) 
    this.porosenko_ru_path = this.d3LinePath(this.porosenko_data.dataRU) 
    this.porohoboty_ua_path = this.d3LinePath(this.porohoboty_data.dataUA)
    this.porohoboty_ru_path = this.d3LinePath(this.porohoboty_data.dataRU) */


   },

  methods: {  
    /* drawPoints: function() { 
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
     }, */
     

     
     //функції відмальовки лайнчартів
    
     /* porosenko_ua_path: function () {   
      var that = this;        
      var newLine =  
      this.d3LinePath(this.porosenko_ua.data) 
      return(newLine) 
    },      */ 
  },
  computed: {    
 /*    porosenko_data: function(){
     var that = this; 
     var maxCount = d3.max(porosenko, function(d) { return +d.count } ); 
     var dates = porosenko.map(function(x) { return new Date(x.week) })
     porosenko.forEach(function(row){ row.week = that.parseDate(row.week) }) 
     var unique_dates = [];
     dates.forEach(function(row){
       if(!unique_dates.includes(row.getTime())){
         unique_dates.push(row.getTime())
       }
     })
     var dataUA = porosenko.filter(function(d){ return d.ua_ === "true" })
     var dataRU = porosenko.filter(function(d){ return d.ua_ === "false" })
     var minDate = new Date(Math.min.apply(null, unique_dates));   
     var maxDate = new Date(Math.max.apply(null, unique_dates));   
     return  { dataUA, dataRU, maxCount, minDate, maxDate }
    },  */
  /*   porohoboty_data: function() {
     var that = this; 
     porohoboty.forEach(function(row){ row.week = that.parseDate(row.week)  })      
     var maxCount = d3.max(porohoboty, function(d) { return +d.count } );      
     var dates = porohoboty.map(function(x) { return new Date(x.week) })
     var unique_dates = [];
     dates.forEach(function(row){
       if(!unique_dates.includes(row.getTime())){
         unique_dates.push(row.getTime())
       }
     })
     console.log(maxCount)
     
     var dataUA = porohoboty.filter(function(d){ return d.ua_ === "true" })     
     var dataRU = porohoboty.filter(function(d){ return d.ua_ === "false" })
     
     dataUA.sort(function(a,b){
       return d3.ascending(a.week, b.week)
     })
     dataRU.sort(function(a,b){
       return d3.ascending(a.week, b.week)
     })
     
     var minDate = new Date(Math.min.apply(null, unique_dates));   
     var maxDate = new Date(Math.max.apply(null, unique_dates));   
     return  { dataUA, dataRU, maxCount, minDate, maxDate }
    }, */

   /*  scale() {
      var that = this; 
      var y = d3.scaleLinear()
        .range([that.height, 0])
       
          
      var x = d3.scaleTime()
        .range([0, that.width])
        .domain([new Date("2013-12-01"), new Date("2020-01-01")])
        return { x, y }; 
    },
    
    
    d3LinePath: function() {
      var that = this;     
      const path = d3.line()
        .x(d => that.scale.x(d.week))
        .y(d => that.scale.y(+d.count));
        return (path) 
    },

     */





    //срач-чарт
     /* leftData: function() {
     data1.map(function(val) {
        val.x = 100+Math.floor(Math.random() * 200);
        val.y = 100+Math.floor(Math.random() * window.innerHeight);
        var theDate = new Date(val.date);
        val.check = theDate.getTime(); 
      })
    return(data1);
    }, */
    /* rightData: function() {
      data2.map(function(val) {
        val.x = 100+Math.floor(Math.random() * 200);
        val.y = 100+Math.floor(Math.random() * window.innerHeight);        
        var theDate = new Date(val.date);
        val.check = theDate.getTime(); 
      })
    return(data2);
    }, */

    /* dates: function(){
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
 */
    /* latest: function() {
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
    }, */
    
    
    /* porosenko_ru_path: function () {   
      var that = this;        
      var newLine = that.d3LinePath(that.porosenko_ru.data) 
      return(newLine)
    },   */
  },
    directives: {    
 /*    axisY(el, binding, vnode) {            

     vnode.context.scale.y.domain(binding.value)      
      d3.select(el).call(d3.axisLeft(vnode.context.scale.y)       
      );
    },
    axisX(el, binding, vnode) {        
      d3.select(el).call(d3.axisBottom(vnode.context.scale.x)
      );
    } */
  }
  }





</script>

<style lang="scss">
@import 'assets/style.scss';


</style>
