<template>
    <div class="contact">
        <div class="contact-form">
            <h1>דברו איתנו</h1>
            <form action="" method="get">
                <input type="text" name="full-name" placeholder="שם מלא">
                <input type="text" name="phone" placeholder="טלפון" required>
                <input type="email" name="email" placeholder="אימייל">
                <textarea id="w3mission" rows="4" cols="50" placeholder="הודעה"></textarea>
                <input type="submit" value="שליחה">
            </form>
        </div>
        <Footer></Footer>
    </div>
</template>

<script>
import Footer from "@/components/Footer.vue";

export default {
  name: "Contact",
  components: {
    Footer      
  }
}
</script>

<style scoped>

    .contact{
        background-color: rgba(0, 86, 97, 0.2);
    }

    .contact-form{
        width: fit-content;
        margin: auto;
        padding: 3rem 0;
    }

    h1{
        font-size: 3rem;
        margin-bottom: 3rem;
    }

    input, textarea{
        display: block;
        text-align: right;
        font-size: 1rem;
        margin: 1.5rem;
        padding: 0.7rem;
        width: 18rem;
    }

    input[type="submit"]{
        background-color: rgb(219, 134, 236);
        color: white;
        border: none;
        font-size: 1.5rem;
        text-align: center;
    }

   input[type="submit"]:hover{
        font-weight: bold;
        cursor: pointer;
        color: #2c3e50;;
    }

    textarea{
        resize: none;
        font-family: 'Alef', sans-serif;
    }

@media (min-width: 52rem)
{
    form{
        max-width: 35rem;
        
    }
    input, textarea{
        display: inline-block;
        margin: 1rem 0.5rem;
        width: 15rem;
    }

    textarea, input[type="submit"], input[name="full-name"]{
        width: 31rem;
    } 
}
  
</style>

