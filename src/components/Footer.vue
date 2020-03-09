<template>
  <div class="footer">
    <div class="contact-us">
      <p>צור קשר</p>
      <form action="" method="get">
        <input type="text" name="name" placeholder="שם" required>
        <input type="email" name="email" placeholder="אימייל" required>
        <input type="submit" value="שלח">
      </form>
    </div>
     <div class="details">
      <p>052-333-20-20</p>
      <p>רוטשילד 49, פתח תקווה</p>
      <p>info@looking-good.com</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer", 
  methods: {
    
    
  }
}
</script>

<style scoped>

  .footer{
    display: block;
    background-color: #2c3e50;
  }

  .contact-us
  {
    margin-top: 2rem;
  }

  .details
  {
    display: grid;
  }

  p{
    color: white;
    display: inline-block;
    font-size: 1.3rem;
    font-weight: bold;
    margin: 0.5rem;
  }

  form{
    width: fit-content;
    margin: 0 auto;
  }

  input{
    display: block;
    font-size: 1rem;
    text-align: right;
    margin: 1rem auto;
    padding: 0.5rem;
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

  @media (min-width: 51rem)
  {
    .footer{
      display: grid;
      grid-template-columns: 50% 50%;
    }
    
    .details{
      display: grid;
      grid-template-rows: 40px 40px 40px;
      margin: auto;
    }
  }
</style>