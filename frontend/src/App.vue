<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import UserLogin from './components/UserLogin.vue';
import DressPicture from '../public/images/girldress.jpeg'
</script>

<template>
  <header>
    <img :src="DressPicture" width="200" class="startingPicture">

    <div class="wrapper">

      <div>
        <UserLogin />
      </div>

      <!-- För VG behöver följande finnas i frontenddelen. 
        1. Möjlighet att skapa ny användare. 
        2. En loginruta. 
        3. Lösenordet ska skickas krypterat. 
        4. Det ska gå att se vilka produkter som finns i butiken, fördelat på olika kategorier. 
        5. Varje produkt ska innehålla grundläggande info som pris, namn och bild. 
        6. Det ska vara möjligt att lägga produkten i en kundvagn. 
        7. Det ska gå och lägga en order med produkterna i kundvagnen. 
        8. Det ska finnas en sida med alla skapade orders samt vilka produkter ordrarna innehåller. 
        9. Inloggning och kundvagn ska sparas i localstorage -->

      <nav>
        <RouterLink to="/orders">Se dina ordrar</RouterLink>
        <RouterLink to="/about">Skapa användare</RouterLink>
        <RouterLink to="/produkter"> Produkter</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  padding: 2rem;
}

.startingPicture {
  margin: 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
