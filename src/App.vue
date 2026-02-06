<script setup>
import ContentStories from './components/ContentStories.vue';
import Minperfil from './components/minperfil.vue';
import NavBar from './components/navBar.vue';
import NavBarmin from './components/navBarmin.vue';
import Publicacione from './components/Publicacione.vue';

</script>

<template>
  <header>
    <div class="wrapper">
    </div>
  </header>

  <main>
    <div class="flex w-full">
      <div class="hidden lg:inline w-1/8 ">
        <NavBar />
      </div>
      <div class="w-full lg:w-9/20">
        <br />
        <ContentStories />
        <Publicacione />
      </div>
      <div class="hidden lg:inline w-3/10 ">
        <Minperfil />
      </div>
      <div class="fixed bottom-0 left-0 w-full lg:hidden">
        <NavBarmin/>
      </div>
    </div>

  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
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
}
</style>
