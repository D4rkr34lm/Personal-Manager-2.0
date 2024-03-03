<script setup lang="ts">
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

const navActiv = ref(false)
</script>

<template>
  <header>
    <button class="ui-button" id="nav-menu-button" @click=" navActiv=!navActiv "><img class="header-icon" src="./assets/icons/speisekarte.png"></button>
    <div class="header-container">
      <img class="fh-icon" src="./assets/icons/fh.png">
      Software: Manganer
    </div>
    <button class="ui-button"><img class="header-icon" src="./assets/icons/einloggen.png"></button>
  </header>
  <nav v-if="navActiv">
    <RouterLink to="/calender" class="nav-link"><img class="nav-icon" src="./assets/icons/kalender.png"> Calender</RouterLink>
    <RouterLink to="/email" class="nav-link"><img class="nav-icon" src="./assets/icons/mail.png"> Email</RouterLink>
    <RouterLink to="/taskboard" class="nav-link"><img class="nav-icon" src="./assets/icons/beschilderung.png"> Taskboard</RouterLink>
  </nav>
  <RouterView/>
  <footer>

  </footer>
</template>

<style scoped>
  header {
    position: relative;
    z-index: 10;

    display: flex;
    flex-direction: row;
    justify-content: space-between;

    padding: 5px;

    height: 8vh;
    background-color: var(--green-2);

    font-size: 7vh;

    box-shadow: 0 0px 5px 0;
  }

  .header-container {
    display: flex;
    height: 100%;
  }

  .header-icon {
    max-width: 5vh;
    max-height: auto;

    margin-right: 10px;
  }

  .ui-button{
    background: none;
    border: none;

    padding-left: 15px;
    padding-right: 3px;

    border-radius: 25px;
  }

  .ui-button:hover {
    background-color: var(--green-1);
  }

  .ui-button:active {
    background-color: var(--green-3);
  }

  nav {
    position: relative;
    z-index: 0;

    width: 5vw;
    min-width: 200px;

    box-shadow: 0 0px 5px 0 grey;
    
    
    background-color: rgb(255, 255, 255);

    min-height: 90vh;
  }

  .nav-icon {
    max-width: 5vh;
    max-height: auto;

    margin-right: 10px;
  }

  .nav-link{
    display: flex;
    flex-direction: row;
    align-items: center;

    padding: 6px;
    margin-bottom: 10px;

    color: black;

    font-size: 3vh;
    text-decoration: none;
  }

  .nav-link:hover {
    background-color: rgb(232, 232, 232);
  }

  .nav-link:active {
    background-color: rgb(205, 205, 205);
  }
  
</style>
