<template>
    <div class="contact">
        <div class="contact-form">
            <form action="" method="get">
                <input type="text" name="name" placeholder="שם פרטי" required>
                <input type="text" name="last-name" placeholder="משפחה">
                <input type="text" name="phone" placeholder="טלפון" required>
                <input type="email" name="email" placeholder="אימייל">
                <textarea id="w3mission" rows="4" cols="50" placeholder="הודעה"></textarea>
                <input type="submit" value="שלח">
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

    .contact-form{
        width: fit-content;
        margin: auto;
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
        background-color: rgb(230, 24, 24);
        color: white;
        border: none;
        width: 7rem;
        text-align: center;
    }

   input[type="submit"]:hover{
        background-color: white;
        color: rgb(230, 24, 24);
        font-weight: bold;
        cursor: pointer;
    }
  
</style>

