<template>
    <div class="container">
        <h1>הצוות שלנו</h1>
        <div class="coaches">
            <Coach v-for="(coach, index) in coachesList" :description="coach.description" :name="coach.name" :img="coach.img" :key.sync="index">
            </Coach>
        </div>
        <Footer></Footer>
    </div>
</template>

<script>

import Coach from "@/components/Coach.vue";
import Footer from "@/components/Footer.vue";

export default {
    name: "Coaches",
    components: {
        Coach, 
        Footer
    },
     data(){
         return{
             coachesList: [
                 {
                    img: "https://images.squarespace-cdn.com/content/v1/5aa543171137a614d706054b/1578947542887-0Y372I8W86UHGEGU14R9/ke17ZwdGBToddI8pDm48kGhebe1P8ATlDh9OeLUmcoF7gQa3H78H3Y0txjaiv_0fDoOvxcdMmMKkDsyUqMSsMWxHk725yiiHCCLfrh8O1z5QHyNOqBUUEtDDsRWrJLTmTl_ALRZE0UkEheIF40jl8nyLDkBqe71l9olrIWQJ2x6z74ojjTp85WyWKI3oT7zw/Cody+Head+Shot.JPG", 
                    name: "דניאל ליבוביץ",
                    description: "אבא, בעל, מתאמן בקרוספיט משנת 2009, מקסימום שבועיים רצוף. הבעלים הבלתי מעורער של קרוספיט נמל"
                 },
                {
                    img: "https://d22ir9aoo7cbf6.cloudfront.net/wp-content/uploads/sites/2/2017/04/honeycombers-personal-trainer-gym-n-tonic.jpg", 
                    name: "דניאל גמליאל",
                    description: "מאמנת פילאטיס - לשיעורים שלה מזמינים תור שלושה חודשים מראש, כמו מסעדה נחשקת. היא כאן לאזן אתכם"
                 },
                 {
                    img: "https://itsxtraliving.com/wp-content/uploads/2019/11/Omer.jpg", 
                    name: "טל עשור",
                    description: "מלך אימוני הסטודיו שלנו, טופ שלוש בתל אביב בקפיצה משולשת, נותן מעצמו מלא ועדיין נשאר בלי סוף, הופך אימונים לחוויות בלתי נשכחות מאז 2008"
                 },
                 {
                    img: "https://cdn.gethypervisual.com/images/shopify/21b431a8-76c1-4054-b108-bb46902d3547/w1200_6325_didie-nturo-1119554-unsplash.jpg", 
                    name: "עומר סוילם",
                    description: "מהנדס בניין, קופץ 300 דאבל אנדרס רצוף, המאמן הכי אינטיליגנטי במערכת השמש, מאמן מכל הלב והנשמה, חבר אמיתי"
                 },
                 {
                    img: "https://static.spacecrafted.com/de02792ecea748989991ead92c8ff426/i/fe2d662ff96340e994365f37943c4616/1/4SoifmQp45JMgBnHp7ed2/TRX-exercises-moves.jpg", 
                    name: "עמית עיני",
                    description: "מלכת הסטודיו, אהובה, חמה, קשובה, אבל גם חזקה, לא נבהלת מכלום וכשהיא מדברת כולם מקשיבים"
                 },
                 {
                    img: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRjzONIvUrL4GtJD1ykqggica1IdrbIzVVe_sf6z-hbMxs3ojui", 
                    name: "יערה נעים",
                    description: "שירות לקוחות - האדם הכי נעים שיצא לכם לפגוש, קסם מהלך שיושב בדלפק ודואג שתכנסו ותצאו בחיוך"
                 },
                 {
                    img: "https://lh3.googleusercontent.com/proxy/deI_kHt2efbCU8GMNZg8pPY4TzakQGZIZD9u1z9rdZPsQG7dHnYIxQ3QvRIn1HqCitW5sXruyUK8YF5S154C0FSuFNOQPT6OXZjbtS3y71qdXTW2HVN5", 
                    name: "רם דובר",
                    description: "אלוף הארץ באליפות הארץ, בכושר גופני ומלך הקרוספיט הבלתי מעורער. לאיש יש יותר תעודות והסמכות ממה שאפשר להכניס פה, אינציקלופדיה של ידע עם ניסיון מוכח"
                 },
                 {
                    img: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcRKPl4DE5VsyY1qTHJWlFJ9rBtNfxRWH-Q5jYhW-7bygTAytt8Q", 
                    name: "ניב גרינבלט",
                    description: "הצעיר בחבורה, נותן מאה עשרים אחוז תמיד, מדבר שוטף גרמנית, עברית, אנגלית, ערבית וממש קצת צרפתית.יש האומרים שהוא חצי אדם חצי נמלה"
                 },
                 {
                    img: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcTq26TyQ4BfAdsNvLyjbhwhTF-OQV8xwIT6dChyOwHOUQA587if", 
                    name: "אבי יונה",
                    description: "איש ענק תרתי משמע, מאמן מלידה, נושם וחי קרוספיט עשור כמעט, סבלני ושליו, ספורט-תרפיסט, ספורטאי תחרותי ואיש מהמם באופן כללי"
                 },
                 {
                    img: "https://cdn1.coachmag.co.uk/sites/coachmag/files/styles/insert_main_wide_image/public/2016/06/push-press-guy2.jpg?itok=LIh8iKi5", 
                    name: "ליאור גזית",
                    description: "הנצר האחרון לבית טרגאריאן, דובי צהוב מפוצץ בכח, אנרגיה וקסם. יוצא יחידה מובחרת שגם מוביל את קבוצת ההכנה לצהל של המועדון"
                 },
                 {
                    img: "https://cdn.gearpatrol.com/wp-content/uploads/2018/12/Trainers-Share-Their-Home-Gym-Essentials-gear-patrol-matt-f.jpg", 
                    name: "עמית אזולאי",
                    description: "יוצא יחידה מובחרת שמתנהל ככזה - חזק, שקט, ממוקד שיודע להשיג תוצאות. קרוספיטר תחרותי טרי שעוד יכבוש את התחום"
                 },
                 {
                    img: "https://previews.123rf.com/images/antoniodiaz/antoniodiaz1807/antoniodiaz180701054/105097112-portrait-of-an-attractive-female-gym-coach-taking-some-notes-and-smiling-at-camera-while-standing-ou.jpg", 
                    name: "לי ביצ'ו",
                    description: "שירות לקוחות - תמיד כאן כשצריך אותה ובדרך כלל, צריך אותה. עזרה לאחרים זה התחביב שלה. חברה פנטסטית"
                 },
                 {
                    img: "https://scontent-atl3-1.cdninstagram.com/v/t51.2885-15/e15/23101316_2006750992937292_5030146159545417728_n.jpg?_nc_ht=scontent-atl3-1.cdninstagram.com&_nc_cat=100&_nc_ohc=oo1tWr7LK-YAX-a7SB9&oh=ea36c655ba6d18bea98999178e6ed793&oe=5E768D50", 
                    name: "מורן לוי",
                    description: "המנהלת של הבוקס - הבוקס בשבילה הוא כמו הבית, העובדים כמו ילדים והמתאמנים כמו משפחה. אלופת ישראל בלגרום לדברים לקרות"
                 }
             ]
         }
     }
};
</script>

<style scoped>

    .coaches{
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        margin: 2rem auto;
        width: fit-content;
    }

    h1{
        font-size: 3rem;
        margin-top: 3rem;
    }

</style>