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
                  <p><a href="#">{{data.description3}}</a></p>

                </div>
              </div>
        
            </div>
          
          <div id="main4">
            <div class="main4-wrap" v-for="(data,index) in contents" :key="index">
                  <div class="main4-top">
                    <div class="main4-inner1">
                      <h2>{{data.title}}</h2>
                       <p>{{data.semiTitle}}</p>
                    </div>
                  </div>

              </div>
    

          </div>


   

    

           


      


    </main>
    <CommonFooter></CommonFooter>
  </div>
  
</template>


<script>
import CommonHeader from "./components/CommonHeader.vue";
import CommonFooter from"./components/CommonFooter.vue";

export default{
   data(){
    return{
      services:[
        {
        img: require("./assets/service2.jpg"),
        title: "web制作事業",
        description1:"コーチングのミッション",
        description2:
        "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります",
        description3:"サービス詳細"

        },
        {
          img: require("./assets/service1.jpg"),
          title: "web制作事業",
          description1:"コーチングのミッション",
          description2:
          "ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります",
          description3:"サービス詳細"
        }  

      ],

      contents:[
        {
          title:"company",
          semiTitle:"会社概要"
        },
        {
          title:"recruit",
          semiTitle:"採用情報"
        }
      ]
    };
  },
  
  components:{
    CommonHeader,
    CommonFooter
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

/* header */
.header-wrap{
  background-color: black;
  color: white;
  height: 60px; 
}

.hamburger{
  position: absolute;
  cursor: pointer;
  top: 10px;
  right: 30px;
  transition: 0.4s;
}

span{
  position: absolute;
  left: 2px;
  display: block;
  width: 35px;
  height: 2px;
  background-color: #fff;
  transition: 0.8s;
}

span:nth-of-type(1){
  top: 10px;
}

span:nth-of-type(2){
  top: 20px;
}

span:nth-of-type(3){
  top: 30px;
}
.header-logo{
  padding-top: 20px;
  padding-left: 30px;
}

.header-nav ul{
  display: none;
}

/* main1 */
.main1-wrap{
  background-image: url(./assets/eyecatch.jpg);
  position: relative;
}

.main1-wrap h2{
  color: white;
  font-style: italic;
  padding: 200px 0;
  text-align: center;
  font-size: 3em;
}
.flex-container1{
  display: flex;
  flex-direction: row;
  position: absolute;
  right: 0%;
  bottom: 0%;
  width: 100%;

}

.flex-item1{
  background-color: white;
  padding-right: 20px;

}

.flex-item2{
  background-color:black;
  color: white;
  font-weight: bold;
  display: flex;
  align-items: center;
  
}

.item1-2{
  padding-left: 1vw;
}

.flex-item2 p{
  padding: 3vh 2vw;
}

/* main2 */

#main2{
  background-color: black;
  position: relative;
  
}
.main2-wrap{
  color: white;
  height: 450px;
  width: 80%;
  margin: 0 auto;
  padding-top: 10%;
}

.title1{
  line-height: 1.5em;
  font-size: 2em;
  font-weight: bold;
}
.title2{
  line-height: 1.5em;
  padding-top: 10%;
  padding-bottom: 10%;
}

.title3{
  margin-top: 3%;
}

.title3 a{
  background-color: white;
  border: 1px solid black;
  text-decoration: none;
  color: black;
  padding: 10px 20px;
  
}

.main2-img img{
  width: 45vw;
  height: 15vh;
  position: absolute;
  right: 30px;
  top: 445px;
  background-size: cover;
}


/* main3 */
#main3{
  margin-top: 10%;
  background-color:#f2f2f2f2;
}

.main3-title{
  font-size: 2em;
  font-weight: bold;
  color: #666666;
  text-align: center;
  padding-top: 5%;
  padding-bottom: 5%;
  
}
.main3-wrap{
  text-align: center;
}
.main3-1{
  width: 85%;
  display: inline-block;
  background-color: white;
  text-align: left;
  
}
.main3-1 img{
  width: 100%;
}



.title3-1-4{
  margin-top: 3%;
  margin-left: 50%;
  border: 1px solid black;
  padding: 10px 20px;
  margin-bottom: 10%;
  margin-right: 5%;
  display: inline-block;
 

}
.title3-1-4 a{
  text-decoration: none;
  color: #000;
  padding: 0 1vw;
  
  
}

.title3-1-1{
  padding-top: 5%;
  padding-left: 5%;
  font-weight: bold;

}
.title3-1-2{
  line-height: 3em;
  padding-left: 5%;
}

.title3-1-3{
  padding-left: 5%;
  padding-right: 3%;
  line-height: 1.5em;
}


.main3-2{
  margin-top: 15%;
  margin-bottom: 15%;
  display: inline-block;
  width: 85%;
  background-color: white;
  text-align: left;
}

.main3-2 img{
  width: 100%;
}

.title3-2-4{
  margin-top: 3%;
  margin-left: 50%;
  border: 1px solid black;
  padding: 10px 20px;
  margin-bottom: 10%;
  margin-right: 5%;
  display: inline-block;
}

.title3-2-4 a{
  text-decoration: none;
  color: #000;
  padding: 0 1vw;
  
  
  
}

.title3-2-1{
  padding-top: 5%;
  padding-left: 5%;
  font-weight: bold;

}
.title3-2-2{
  line-height: 3em;
  padding-left: 5%;
}

.title3-2-3{
  padding-left: 5%;
  padding-right: 3%;
  line-height: 1.5em;
}

/* main4 */
.main4-wrap{
  display: flex;
  flex-wrap: wrap;
  margin-top: 10%;
}
.main4-top{
  background-image: url(./assets/eyecatch.jpg);
  color: white;
  width: 100%;
  height: 300px;
  position: relative;
}

.main4-inner1{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.main4-inner1 h2{
  font-size: 2.5em;
}
.main4-inner1 p{
  font-weight: bold;
  font-size: 1.5em;
  text-align: center;
  padding-top: 10%;
}

.main4-bottom{
  background-image: url(./assets/recruit.jpg);
  color: white;
  width: 100%;
  background-position: center;
  height: 300px;
  position: relative;
}
.main4-inner2{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.main4-inner2 h3{
  font-size: 2.5em;
}
.main4-inner2 p{
  font-weight: bold;
  font-size: 1.5em;
  text-align: center;
  padding-top: 10%;
}

/* main5 */
.flex-container5{
  display: flex;
  background-color: #000;
  color:white;
  width: 90%;
  justify-content: center;
  margin: 10% auto;
  align-items: baseline;

}

.flex-item5-1{
  font-size: 2em;
  font-weight: bold;
  padding-top: 20%;
  padding-bottom: 20%;
  padding-left: 10%;
  flex-grow: 1;

}

.flex-item5-2{
  font-size: 1.3em;
  flex-grow: 3;
  
  
  
}

/* main6 */
#main6{
  background-image: url(./assets/eyecatch.jpg);
  color: #fff;
}

.main6-wrap{
  text-align: center;
  padding-left: 10%;
  padding-right: 10%;
  
}

.main6-wrap h4{
  font-size: 2em;
  padding-top: 10%;
}

.main6-1{
  line-height: 2em;
  font-weight: bold;
}

.main6-2{
  font-size: 3em;
  padding-top: 5%;
}

.main6-3{
  padding-top: 10%;
  line-height: 1.5em;
}
.main6-4{
  padding-top: 10%;
  padding-bottom: 10%;
}
.main6-4 a{
  text-decoration: none;
  color: white;
  border: 1px solid white;
  padding: 2vh 4vw;
}

h5{
  color: white;
  background-color: black;
  text-align: center;
  line-height: 3em;
}



footer{
  color: white;
  background-color: black;
  text-align: center;
}



@media screen and (max-width: 767px){
  .header-nav2{
  display: none;
}

.flex-item5-1{
  text-align: center;
}
.flex-item5-2{
  text-align: center;
}
.flex-container1{
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    position: absolute;
    right: 0%;
  }

}
@media screen and (min-width: 768px){
  .hamburger{
    display: none;
  }

  .header-wrap{
    display: flex;
    justify-content: space-between;
  }

  .header-nav{
    display: flex;
    align-items: center;

  }
  .header-nav ul{
    display: flex;
    list-style: none;
    justify-content: space-around;
    
  }
  .header-nav li{
      margin-right: 35px;
  }

  .header-nav a{
    color: white;
    text-decoration: none;
  }

 /* main1 */

 .main1-wrap h2{
   display: inline-block;
   padding-top: 40%;
   padding-left: 10%;
   background-image: center;
 }
  
 .main1-wrap{
   position: relative;
 }
  
  .flex-container1{
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    position: absolute;
    right: 0%;
  }

  /* main2 */
  
  .title1{
    font-size: 1.5em;
    position: relative;
    z-index: 3;
  }
  .title2{
    padding-top: 3%;
    padding-bottom: 3%;
    position: relative;
    z-index: 2;
  }

  .main2-img img{
    width: 50%;
    height: 50%;
    position: absolute;
    right: 5%;
    top: 20%;
    z-index: 1;
  }

  /* main3 */
  .main3-wrap{
    
  }
  .main3-1{
    position: relative;
    width: 100%;
    background-color: #f2f2f2;
  }
  .main3-1 img{
    width: 50%;
    position: absolute;
    right: 0;
  }
  .contain2{
    margin-top: 5%;
    margin-left: 15%;
    background-color: white;
    position: relative;
    z-index: 1;
    width: 40%;
    height: 33vh;
    
  }

  .title3-1-4 a{
    display: block;
  }
 
  .main3-2 img{
    width: 50%;
    display: inline-block;
    height: 300px;
    background-size: cover;
  }
  
  .main3-2{
    width: 100%;
    background-color: #f2f2f2;
    position: relative;
  }

  .contain3{
    width: 40%;
    background-color: white;
    position: absolute;
    top: 10%;
    left: 40%;
    height: 33vh;

  }

 /* main4 */

 .main4-wrap{
  display: flex;
  justify-content: space-between;
  }

  .main4-top{
    width: 48%;
  }

  .main4-bottom{
    width: 48%;
  }
  
  /* main5 */
  .flex-item5-1{
    padding-top: 5%;
    padding-bottom: 5%;
    
    }

    .flex-item5-2{
      padding-left: 10%;
    }
   
  /* main7 */
  .main-wrap7{
    display: flex;
    justify-content: space-between;
    background-color: black;
    align-items: center;
  }

  .header-nav2 ul{
    display: flex;
    list-style: none;
   
  }

  .header-nav2 li{
    margin-right: 10px;

  }
  .header-nav2 a{
    text-decoration: none;
    color: white;
  }


}



</style>
