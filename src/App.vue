<template>
  <div id="app">
    <CommonHeader></CommonHeader>
    <main>
        <div id="main1">
          <div class="main1-wrap">
            <h2>機械ではできない仕事を</h2>
            <div class="flex-container1">
              <div class="flex-item1">
              <p class="item1-1">2019/01/01</p>
              <p class="item1-2">ニュースタイトルがここに入ります。３月の決算報告書</p>
              </div>
              <div class="flex-item2">
              <p>news</p>
               </div>

            </div>
          </div>
        </div>

        <div id="main2">
            <div class="main2-wrap">
              <div class="title1">
               お客さまのために進化する成長企業であり続ける
              </div>
             <div class="title2">
              顧客主導型サービスを提供する企業として、お客様の会社経営に必要なサービスと情報を提供し続ける企業支援会社を目指します。企業が現在直面している「勝ち残るため」の戦略を提供できる会社として、ホームページをはじめ、各種各種マーケティングをご提供いたします。
             </div>
              <div class="title3">
              <p><a href="#">ミッション詳細</a></p>
            </div>
            <div class="main2-img">
              <img src="./assets/mission-img.jpg">
            </div>
          </div>
        </div>

         <div id="main3">
              <p class="main3-title">service</p>
              <div class="main3-wrap">
                <div class="service-cat" v-for="(data,index) in services" :key="index">
                  <img :src="data.img" alt/>
                  <h1>{{data.title}}</h1>
                  <p>{{data.description1}}</p>
                  <p>{{data.description2}}</p>

                </div>
              </div>
        
            </div>


   

    

           


      


    </main>
  </div>
  
</template>


<script>
import CommonHeader from "./components/CommonHeader.vue";
export default{
   data(){
    return{
      services:[
        {
        img: require("./assets/service2.jpg"),
        title: "web制作事業",
        description1:"コーチングのミッション",
        description2:
        "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります"

        }
        

      ]
    };
  },
  
  components:{
    CommonHeader
  }
}


</script>

<style scoped>

html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
  margin:0;
  padding:0;
  border:0;
  outline:0;
  font-size:100%;
  vertical-align:baseline;
  background:transparent;
}

body {
  line-height:1;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
  display:block;
}

nav ul {
  list-style:none;
}

blockquote, q {
  quotes:none;
}

blockquote:before, blockquote:after,
q:before, q:after {
  content:'';
  content:none;
}

a {
  margin:0;
  padding:0;
  font-size:100%;
  vertical-align:baseline;
  background:transparent;
}

/* change colours to suit your needs */
ins {
  background-color:#ff9;
  color:#000;
  text-decoration:none;
}

/* change colours to suit your needs */
mark {
  background-color:#ff9;
  color:#000;
  font-style:italic;
  font-weight:bold;
}

del {
  text-decoration: line-through;
}

abbr[title], dfn[title] {
  border-bottom:1px dotted;
  cursor:help;
}

table {
  border-collapse:collapse;
  border-spacing:0;
}

/* change border colour to suit your needs */
hr {
  display:block;
  height:1px;
  border:0;
  border-top:1px solid #cccccc;
  margin:1em 0;
  padding:0;
}

input, select {
  vertical-align:middle;
}


</style>
