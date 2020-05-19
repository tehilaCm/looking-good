<template>
  <div class="home">
    <Slider></Slider>
    <div class="about-us">
      <h1>אודותינו</h1>
      <div>
        <span class="logo">Looking good is Feeling good</span> 
        <br>
        <br>
        <p>
          זהו הסטודיו להתעמלות הגדול הישראל ובו כ-900 שיעורי סטודיו בחודש. בסטודיו ניתן למצוא שעורים
          לנשים בלבד ושעורים מעורבים. מגוון השיעורים הגדול כולל שעורים מסוגים שונים וברמות שונות, כך שכל מתעמלת ומתעמל יכולים למצוא את השיעורים המתאימים להם ובזמן המתאים להם
        </p>
        <p>
        <span>חדר כושר מודרני</span>-חדר הכושר של המועדון מכיל את הציוד הטוב ביותר של חדרי הכושר. המועדון מעוצב באופן נעים ומזמין וצוות המדריכים נכון להדריך ולכוון את המעמלים
        </p>
        <p>
          <span>ספינינג</span>-חדר הספינינג של המועדון כולל אופניים של חברת ספיניג עצמה. שעורי הספינינג מתקיימים בשעות שונות מידי יום וצוות המדריכים של המועדון הוא מהטובים ביותר שיש
        </p>
        <p>
          <span>אימון מעגל</span>-אימון מחזורי עם מכשירים הפועלים על התנגדות הידראולית, בשילוב תחנות פעולה אישיות של כוח ואירובי
        </p>
        <br>
        <p>
          הוקם על-פי חזונה של שירן גרין. אשר החליטה להקים מועדון הקשוב לצרכים של המתעמלים, מועדון מכוון מקצועיות חסרת פשרות, שרות מעולה ואוירה חברית
        </p>
      </div>
    </div>
    
    <div class="curses">
      <hr>
      <h1>קורסים</h1>
      <div class="curses-list">
         <Curse v-for="curse in curses" :name="curse.name" :img="curse.img" :key.sync="curse.id">
        </Curse>
        <router-link to="/curses">
        <button>
          לכל הקורסים
        </button>
        </router-link>
      </div>
     
    </div>
    <Footer></Footer>
  </div>
</template>

<script>

import Slider from "@/components/Slider.vue";
import Curse from "@/components/Curse.vue";
import Footer from "@/components/Footer.vue";

export default {
  
  name: "Home",
  components: {
    Slider,
    Curse,
    Footer      
  }, 
   data(){
    return{
          curses: [
          {
              id: "1",
              img: "home - pilates",
              name: "פילאטיס מזרן"
          },
          {
              id: "2",
              img: "home - zumba",
              name: "זומבה"
          },
          {
              id: "3",
              img: "home - bodyShape",
              name: "עיצוב הגוף"
          },
          {
              id: "4",
              img: "home -trampoline",
              name: "טרמפולינה"
          },
          {
              id: "5",
              img: "home - kikbox",
              name: "קיקבוקס"
          },
          {
              id: "6",
              img: "home - bodyPower",
              name: "בודי פאוור"
          }
        ]
      }
    }
};

</script>

<style scoped>
  
  .about-us{
    height: fit-content;
    background-color: rgb(218, 212, 212);
    padding: 3rem;
  }
  
  h1{
      color: #2c3e50;
      margin-bottom: 2rem;
  }

  .about-us div{
    max-width: 60rem;
    margin: auto;
  }

  .about-us p{
      color: #2c3e50;
      text-align: right;
      font-size: 1.1rem;
      padding: 0.5rem;
  }

  .about-us span{
    text-align: right;
    font-size: 1.1rem;
    font-weight: bold;
  }

  .logo{
    color: rgb(230, 24, 24);
    float: right;
    padding: 0.5rem;
  }

  hr{
      width: 95%;
      height: 0.2rem;
      background: #2c3e50;
      margin: 5rem auto 2rem;
  }

  .curses-list{
    margin: auto;
    max-width: 75rem;
  }

  button{
    background-color: rgb(219, 134, 236);
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: block;
    font-size: 1.2rem;
    font-weight: bold;
    margin: 2rem auto 5rem auto;
    cursor: pointer;
    outline: none;
    border-radius: 0.7rem;
  }

  a{
    text-decoration: none;
  }

  button:hover{
    font-size: 1.5rem; 
    margin: 2rem auto 4.6rem auto; 
  }

</style>