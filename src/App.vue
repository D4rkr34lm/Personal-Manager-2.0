<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <button class="ui-button" id="nav-menu-button"><img class="header-icon" src="./assets/icons/speisekarte.png"></button>
    <div class="header-container">
      <img class="fh-icon" src="./assets/icons/fh.png">
      Software: Manganer
    </div>
    <button class="ui-button"><img class="header-icon" src="./assets/icons/einloggen.png"></button>
  </header>
  <nav>
    
  </nav>
  <footer>

  </footer>
</template>

<style scoped>
  
  
  header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    padding: 5px;

    height: 8vh;
    background-color: var(--green-2);

    font-size: 7vh;
    color: black;

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
  
  footer {
    background-color: var(--green-5);
  }

  
</style>
