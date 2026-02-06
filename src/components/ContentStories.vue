<script setup>
import { ref } from 'vue';
import StoriesBar from './StoriesBar.vue';
const stories = ref([
    { id: 1, nombre: "Empanada", ftperfil: "https://calamary.vercel.app/logo.png", storie: true },
    { id: 2, nombre: "Empanada1", ftperfil: "https://pbs.twimg.com/profile_images/501046546943582208/fT9aK-Hi_400x400.jpeg", storie: true },
    { id: 3, nombre: "Empanada2", ftperfil: "https://pbs.twimg.com/media/CWjzsceU8AQe76i?format=jpg&name=medium", storie: true },
    { id: 4, nombre: "Empanada3", ftperfil: "https://pbs.twimg.com/media/EOFJqENUcAYkTZV?format=jpg&name=4096x4096", storie: true },
    { id: 5, nombre: "Empanada4", ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium", storie: true },
    { id: 6, nombre: "Empanada5", ftperfil: "https://pbs.twimg.com/media/D7Y76oGUIAATw2e?format=jpg&name=4096x4096", storie: true },
    { id: 7, nombre: "Empanada6", ftperfil: "https://pbs.twimg.com/media/D4mrCZ5UIAA21HF?format=jpg&name=4096x4096", storie: true },
    { id: 8, nombre: "Empanada7", ftperfil: "https://pbs.twimg.com/media/C0laTnvVQAAotwk?format=jpg&name=large", storie: true },
    { id: 9, nombre: "Empanada8", ftperfil: "https://pbs.twimg.com/media/FFUvtVQacAA51pl?format=jpg&name=4096x4096", storie: true },
    { id: 10, nombre: "Empanada9", ftperfil: "https://pbs.twimg.com/media/EFo-j87UcAM7OZo?format=jpg&name=4096x4096", storie: true },
    { id: 11, nombre: "Empanada10", ftperfil: "https://pbs.twimg.com/media/CwlI8OJVEAEUigq?format=png&name=large", storie: true },
    { id: 12, nombre: "Empanada11", ftperfil: "https://pbs.twimg.com/media/Cn8gYt9UMAABzT0?format=jpg&name=900x900", storie: true },
    { id: 13, nombre: "Empanada12", ftperfil: "https://pbs.twimg.com/media/C0h8qZFUAAAWSCL?format=jpg&name=large", storie: true },
    { id: 14, nombre: "Empanada13", ftperfil: "https://calamary.vercel.app/logo.png", storie: true },
    { id: 11, nombre: "Empanada10", ftperfil: "https://pbs.twimg.com/media/CwlI8OJVEAEUigq?format=png&name=large", storie: true },
    { id: 12, nombre: "Empanada11", ftperfil: "https://pbs.twimg.com/media/Cn8gYt9UMAABzT0?format=jpg&name=900x900", storie: true },
    { id: 13, nombre: "Empanada12", ftperfil: "https://pbs.twimg.com/media/C0h8qZFUAAAWSCL?format=jpg&name=large", storie: true },
    { id: 14, nombre: "Empanada13", ftperfil: "https://calamary.vercel.app/logo.png", storie: true },
    { id: 13, nombre: "Empanada12", ftperfil: "https://pbs.twimg.com/media/C0h8qZFUAAAWSCL?format=jpg&name=large", storie: true },
    { id: 14, nombre: "Empanada13", ftperfil: "https://calamary.vercel.app/logo.png", storie: true },
    

])

</script>
<template>
  <StoriesBar :items="stories" />
</template>