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
                    img: "Daniel.l", 
                    name: "דניאל ליבוביץ",
                    description: "אבא, בעל, מתאמן בקרוספיט משנת 2009, מקסימום שבועיים רצוף. הבעלים הבלתי מעורער של קרוספיט נמל"
                 },
                {
                    img: "Daniel.G", 
                    name: "דניאל גמליאל",
                    description: "מאמנת פילאטיס - לשיעורים שלה מזמינים תור שלושה חודשים מראש, כמו מסעדה נחשקת. היא כאן לאזן אתכם"
                 },
                 {
                    img: "Tal", 
                    name: "טל עשור",
                    description: "מלך אימוני הסטודיו שלנו, טופ שלוש בתל אביב בקפיצה משולשת, נותן מעצמו מלא ועדיין נשאר בלי סוף, הופך אימונים לחוויות בלתי נשכחות מאז 2008"
                 },
                 {
                    img: "Omer", 
                    name: "עומר סוילם",
                    description: "מהנדס בניין, קופץ 300 דאבל אנדרס רצוף, המאמן הכי אינטיליגנטי במערכת השמש, מאמן מכל הלב והנשמה, חבר אמיתי"
                 },
                 {
                    img: "Amit", 
                    name: "עמית עיני",
                    description: "מלכת הסטודיו, אהובה, חמה, קשובה, אבל גם חזקה, לא נבהלת מכלום וכשהיא מדברת כולם מקשיבים"
                 },
                 {
                    img: "Yaara", 
                    name: "יערה נעים",
                    description: "שירות לקוחות - האדם הכי נעים שיצא לכם לפגוש, קסם מהלך שיושב בדלפק ודואג שתכנסו ותצאו בחיוך"
                 },
                 {
                    img: "Ram", 
                    name: "רם דובר",
                    description: "אלוף הארץ באליפות הארץ, בכושר גופני ומלך הקרוספיט הבלתי מעורער. לאיש יש יותר תעודות והסמכות ממה שאפשר להכניס פה, אינציקלופדיה של ידע עם ניסיון מוכח"
                 },
                 {
                    img: "Niv", 
                    name: "ניב גרינבלט",
                    description: "הצעיר בחבורה, נותן מאה עשרים אחוז תמיד, מדבר שוטף גרמנית, עברית, אנגלית, ערבית וממש קצת צרפתית.יש האומרים שהוא חצי אדם חצי נמלה"
                 },
                 {
                    img: "Avi", 
                    name: "אבי יונה",
                    description: "איש ענק תרתי משמע, מאמן מלידה, נושם וחי קרוספיט עשור כמעט, סבלני ושליו, ספורט-תרפיסט, ספורטאי תחרותי ואיש מהמם באופן כללי"
                 },
                 {
                    img: "Lior", 
                    name: "ליאור גזית",
                    description: "הנצר האחרון לבית טרגאריאן, דובי צהוב מפוצץ בכח, אנרגיה וקסם. יוצא יחידה מובחרת שגם מוביל את קבוצת ההכנה לצהל של המועדון"
                 },
                 {
                    img: "Amit.A", 
                    name: "עמית אזולאי",
                    description: "יוצא יחידה מובחרת שמתנהל ככזה - חזק, שקט, ממוקד שיודע להשיג תוצאות. קרוספיטר תחרותי טרי שעוד יכבוש את התחום"
                 },
                 {
                    img: "Li", 
                    name: "לי ביצ'ו",
                    description: "שירות לקוחות - תמיד כאן כשצריך אותה ובדרך כלל, צריך אותה. עזרה לאחרים זה התחביב שלה. חברה פנטסטית"
                 },
                 {
                    img: "Moran", 
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