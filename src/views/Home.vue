<template>
  <div class="home">
    <Slider></Slider>
    <div class="about-us">
      <h1>אודותינו</h1>
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
              img: "https://spt-fitness.co.il/wp-content/uploads/2017/12/pilates2.jpg",
              name: "פילאטיס מזרן"
          },
          {
              id: "2",
              img: "https://hydro.org.il/wp-content/uploads/2015/12/zumba.jpg",
              // data:image/jpeg;base64,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
              name: "זומבה"
          },
          {
              id: "3",
              img: "https://media.self.com/photos/57d88992f71ce8751f6b48f1/master/w_1600%2Cc_limit/plank.jpg",
              name: "עיצוב הגוף"
          },
          {
              id: "4",
              img: "https://thumbs.dreamstime.com/b/trampoline-training-street-sports-performances-outdoor-fitness-training-trampoline-training-street-orenburg-russia-156962126.jpg",
              name: "טרמפולינה"
          },
          {
              id: "5",
              img: "https://sfilev2.f-static.com/image/users/440514/ftp/my_files/4-1.jpg",
              name: "קיקבוקס"
          },
          {
              id: "6",
              img: "https://static.independent.co.uk/s3fs-public/thumbnails/image/2017/10/16/15/weightlifting-champions-picture-id519275554-1.jpg",
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