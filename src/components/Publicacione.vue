<script setup>
import { ref } from 'vue';
import Publicacion from './publicacion.vue';

const publicaciones = ref([
    {
        id: 1,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/D7Y76oGUIAATw2e?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false
    },
    {
        id: 2,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G6WMAOMbAAAEEu_?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 3,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G6V8S8BbMAAtvkV?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 4,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G5yDeO7bMAAr7dd?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 5,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/GZMveNcbAAASnn4?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 6,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G4p9kRnbEAAciCp?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 7,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://calamary.vercel.app/logo.png",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 8,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G4F4PLVWUAEzYYw?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 9,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G3hts5SWAAA_ZxM?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 10,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/G290athbwAIWHWy?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },
    {
        id: 11,
        usuario: "Empanada",
        tiempo: "4h",
        descripcion: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
        ftperfil: "https://pbs.twimg.com/media/CX_B-JGUAAAvh_S?format=jpg&name=medium",
        ft: "https://pbs.twimg.com/media/Gy8s94BbkAA5bC-?format=jpg&name=4096x4096",
        hst: "",
        likes: 125,
        coments: 4,
        expandido: false

    },

])

</script>
<template>
    <!-- <StoriesBar :items="stories" /> -->
    <Publicacion :items="publicaciones" />
</template>