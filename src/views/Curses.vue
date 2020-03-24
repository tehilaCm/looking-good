<template>
  <div class="container">
    <h1>קורסים</h1>
     <div class="curses">
        <CurseForPage v-for="(curse, index) in curses" :description="curse.description" :name="curse.name" :img="curse.img" :key.sync="index">
        </CurseForPage>
      </div>
      <Footer></Footer>
  </div>
</template>

<script>
  import Footer from "@/components/Footer.vue";
  import CurseForPage from "@/components/CurseForPage.vue";

  export default {
  name: "Curses",
  components: {
      CurseForPage,
      Footer
    },
    data(){
      return{
        curses: [
          {
            img: "https://megasport.co.il/media/clnews/x/1545136296497183094.jpg",
            name: "CrossFit",
            description: "אימון קרוספיט נותן מענה בספקטרום רחב של מאפייני כושר גופני: סיבולת לב-ריאה, סיבולת שריר, כוח גמישות, עוצמה, מהירות, קורדינציה, זריזות, שיווי-משקל ודיוק. את התוכנית שלנו אנחנו מכינים בקפידה על ידי צוות מדריכים מנוסים שבוחנים ובודקים את האימונים לפני הביצוע שלהם למתאמנים בפועל"
          },
          {
            img: "data:image/jpeg;base64,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",
            name: "יוגה",
            description: "השיעורים משלבים את זרמי האשטאנגה וויניאסה יוגה, ומפתחים גמישות ורכות מול עוצמה וכוח. השיעורים דינמיים ואקטיביים ובהם שמים דגש על הנשימה ותנועה אשר יוצרת גמישות, ויטאליות וחוזק"
          },
           {
            img: "https://amp.thenational.ae/image/policy:1.719801:1523202284/lf09-APR-fitness.jpg?f=16x9&w=1200&$p$f$w=5dce02a",
            name: "Burn",
            description: "אימון פונקציונלי בעל תכונות מורכבות המדמה פעילות יומיומית. האימון מתאפיין באינטנסיביות גבוהה, תרגילי כוח ותנועה, משלב עבודה על כמה קבוצות שרירים יחד ויוצר שיפור בכל מרכיבי הכושר הגופני. מטרת האימון לשמור על דופק גבוה לאורך זמן - תוך דגש על תנועה נכונה"
          },
          {
            img: "https://pilatesabadell.com/wp-content/uploads/2017/09/pilates_matt_web.jpg",
            name: "פילאטיס מזרן",
            description: "משלב את עולם הקונטרלוג'י - שיטתו המקורית של ג'וזף פילאטיס. בתוך השקפה כי הגוף ראוי להתייחסות, הנעת רקמות, יצירת תנועה וזרימה. שיעור יגע במנחים שונים, נשימה נכונה ומדיטציה"
          },
          {
            img: "https://yegfitness.ca/wp-content/uploads/2019/10/reformer-pilates-e1571591708338.jpg",
            name: "פילאטיס מכשירים",
            description: "פילאטיס בשילוב מכשירים שונים כגון מיטות אימון. העבודה על המכשירים מחזקת את השרירים ומאתגרת ביותר"
          },
          {
            img: "https://uploads.thealternativepress.com/uploads/photos/best_f1fdbea9077ac021e2a9_Zumba__-_smiling_women_2.jpg",
            name: "זומבה",
            description: "שיעורי זומבה הם למעשה אירובי דאנס המשלב מוזיקה מדרום אמריקה יחד עם צעדי ריקוד לטיניים ובינלאומיים, כמו סלסה, רומבה, צ'ה צ'ה, סמבה, טנגו וכו. צעדי הריקוד נלמדים משיעור לשיעור. הריקודים נלמדים בכל שיעורים וחוזרים בשיעורים הבאים – כל אחת יכולה ללמוד את הצעדים"
          },
           {
            img: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQ3Ax13B-yhoFRyLVk3fThksfRWiFFHJ4TSEZa7xqIhvJrgDwiw",
            name: "עיצוב הגוף",
            description: "שיעור עיצוב לחיזוק השרירים בעזרת אביזרים: כדור, גומיות, בר וחזרה על תרגילים המשפרים יציבה , מסייעים בחיזוק הגוף, ונותנים דגש על כוח"
          },
          {
            img: "https://ae01.alicdn.com/kf/HTB1e7pHeoKF3KVjSZFEq6xExFXav/48-Inch-Hexagonal-Muted-Fitness-Trampoline-with-Adjustable-Handrail-for-Indoor-GYM-Jump-Sports-Adults-Kids.jpg_640x640q70.jpg",
            name: "טרמפולינה",
            description: "בשיעור זה כל מתאמן עובד על טרמפולינה אישית. רוב השיעור מתבצע על הטרמפולינה תוך ביצוע תרגילים אינטנסיביים ומהירים. מטרת השיעור היא עבודה על סבולת לב ריאה וחיזוק השרירים. השיעור מומלץ מאוד ואף מסייע בחיטוב הגוף"
          },
           {
            img: "https://cdn.mos.cms.futurecdn.net/bDjGpjAESLrZUuLYKrRYFC-768-80.jpg",
            name: "בודי פאוור",
            description: "שיעור חדשני המשלב בין עולם חדר הכושר לסטודיו. בשיעור נעשה שימוש במשקולות ומוטות באופן דומה לעבודה בחדר הכושר. מטרת השיעור היא חיזוק הגוף ועבודה איטית ונכונה על כל קבוצות השרירים העיקריות בגוף"
          },
          {
            img: "https://cdn.shopify.com/s/files/1/0072/3304/4541/files/Is-cardio-kickboxing-good-for-weight-loss.jpg?v=1554986399",
            name: "קיקבוקס",
            description: "הקיקבוקס הוא שיעור אירובי בסטודיו הלקוח מתוך שיטת הלחימה טקוואנדו, מטרת השיעור היא שריפת קלוריות מרבית וחיזוק והגמשת הגוף. השיעור מתבסס על תנועות האגרוף תוך שילוב של עבודת אירובי"
          }
        ]
      }
    },
    created() {

            window.scrollTo(0,0);
    }
  }
</script>

<style scoped>

  .curses{
    margin: 2rem auto;
  }

  h1{
    font-size: 3rem;
    margin-top: 3rem;
  }

  @media(min-width: 51rem)
  {
    .curses{
      display: flex;
      flex-wrap: wrap;
    }
  }

</style>