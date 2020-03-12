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
        <!-- כפתור שאר קורסים -->
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

</style>