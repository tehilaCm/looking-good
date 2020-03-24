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
                    img: "https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcT48Mp0KMnlFbbkW1a2vN5i7vspprzsI0SI0Ekj8fM2QHNQYFbC", 
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
                    img: "data:image/jpeg;base64,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", 
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