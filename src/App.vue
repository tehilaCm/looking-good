<template>
  <div id="app">
   <div class="nav">
      <div class="icon">
          <img :src="require('@/assets/logo.png')">
      </div>
      <div class="logo-part-1 logo-style">
        <p>Looking</p>
        <p>Feeling</p>
      </div>
      <div class="logo-part-2 logo-style">
        <p class="good">Good</p>
      </div>
      <img :src="require('@/assets/menu.png')" class="mobile-nav-icon" @click="openMobileNav()">
      <div class="mobile-nav_items">
        <p class="close" @click="closeMobileNav()">X</p>
        <router-link to="/">דף הבית</router-link>
        <router-link to="/">הצוות שלנו</router-link> 
        <router-link to="/about">קורסים</router-link>
        <router-link to="/">מערכת שעות</router-link> 
        <router-link to="/about">צור קשר</router-link>
      </div>
      <div class="nav_items">
        <router-link to="/">דף הבית</router-link>
        <router-link to="/">הצוות שלנו</router-link> 
        <router-link to="/about">קורסים</router-link>
        <router-link to="/">מערכת שעות</router-link> 
        <router-link to="/about">צור קשר</router-link>
      </div> 
    </div>
    <router-view />
  </div>
</template>

<script>
 
    export default {
    name: "App",
    methods: {
    openMobileNav: function(){
      let mobileNavItems = document.querySelector(".mobile-nav_items");
      let mobileNavIcon = document.querySelector(".mobile-nav-icon");
      mobileNavItems.style.opacity = "1"; 
      mobileNavItems.style.trasform = "translateY(0)";
      mobileNavItems.style.zIndex = "2"; 
      mobileNavIcon.style.visibility = "hidden"
    },
     closeMobileNav: function(){
      let mobileNavItems = document.querySelector(".mobile-nav_items");
      let mobileNavIcon = document.querySelector(".mobile-nav-icon");
      mobileNavItems.style.opacity = "0"; 
      mobileNavItems.style.zIndex = "-1"; 
      mobileNavIcon.style.visibility = "visible"

      setTimeout(()=>{ 
        mobileNavItems.style.zIndex = "-1"; 
      },1000);
    }
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  .nav{
    display: flex; /*grid*/
    /* grid-template-columns: 6rem 6rem; */
    width: 100%;
  }

   .mobile-nav_items{
    width: 13rem;
    height: 100%;
    display: block;
    margin-top: 3rem;
    position: fixed;
    right: 0;
    z-index: -1;
    background-color: rgb(240, 240, 228);
    opacity: 0;
    transform: translateY(-3rem);
    transition: opacity 1s, transform 1s;
  }

  .mobile-nav_items a{
    display: block;
    margin: 1rem;
    text-decoration: none;
    font-weight: bold;
    color: #2c3e50;
    cursor: pointer;
  }

  .mobile-nav_items a:hover{
    color: rgb(230, 24, 24);
  } 

  .close{
    display: block;
    text-align: right;
    font-weight: bold;
    font-size: 1.3rem;
    margin: 1rem;
    cursor: pointer;
  }

  .close:hover{
    color: rgb(230, 24, 24);
  }
  
  .nav_items{
    display: none;
  }

  .mobile-nav-icon{
    width: 2rem;
    height: 2rem;
    right: 1rem;
    margin: 1.7rem 0rem;
    position: absolute;
    cursor: pointer;
  }

 .logo-part-1{
    margin: 1rem 0.5rem 1.7rem 1rem;
    font-size: 1.2rem;
    /* grid-column-start: 1; */
  }

  .logo-part-1 p{
      margin: 0 auto;
    }

  .logo-part-2{
    margin-top: 0.6rem;
    font-size: 2rem;
    vertical-align: center;
  }

  .logo-style{
    color: #2c3e50;
    font-weight: bold;
    font-family: 'Lato', sans-serif;
  }

  .good{
    margin-top: 0.8rem;
    margin-right: 7rem;
  }

  .nav_items a:hover {
     color: rgb(230, 24, 24);
    } 

  .icon{
    vertical-align: middle;
    margin-left: 1rem;
  }
 
  img{
    width: 4rem;
    margin-top: 0.5rem;
  }

@media (min-width: 51rem)
{
  .nav{
    display: flex;
  }

  .mobile-nav_items{
    display: none;
  }

  .nav_items {
    padding: 40px 10px;
    width: 80%;
    text-align: right;
    display: block;
  }

  .nav_items a {
    font-weight: bold;
    color: #2c3e50;
    margin: 0 1rem;
    text-decoration: none;
    }

  .nav_items a.router-link-exact-active {
    /* color: rgb(230, 24, 24); */
  }

  .mobile-nav-icon{
    display: none;
  }

.logo-part-1{
  margin-top: 1rem;
}

.logo-part-2{
    font-size: 3rem;
    margin-top: 0rem;
    margin-right: 0;
  }

  .good{
    margin-right: 0;
  }
}
</style>
