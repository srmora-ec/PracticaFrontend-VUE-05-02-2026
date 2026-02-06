<script setup>
import { onMounted, ref } from 'vue';
import Preperfil from './preperfil.vue';

const props = defineProps({
    items: {
        type: Array,
        required: true,
        default: () => []
    }
});

</script>

<template>

    <div class="flex flex-col items-center relative w-full">
        <ul class="w-full max-w-md">
            <li v-for="publicacion in props.items" :key="publicacion.id" class="flex flex-col pt-5 md:p-3 md:pt-0">
                <div class="flex">
                    <div class="flex gap-1 items-center w-full ">
                        <div href="#" class="p-3 cursor-pointer group">
                            <img :src="publicacion.ftperfil" class="w-8 h-8 rounded-full" />
                            <div class="absolute flex items-center justify-center cursor-pointer invisible 
              group-hover:visible opacity-100  delay-800 w-3/5">
                                <Preperfil :item="publicacion" />
                            </div>
                        </div>
                        <div href="#" class="cursor-pointer group">
                            <p class="text-white font-black">
                                {{ publicacion.usuario }}
                            </p>
                            <div class="absolute  z-8 flex items-center justify-center cursor-pointer invisible
              group-hover:visible opacity-100  delay-800 w-3/5">
                                <Preperfil :item="publicacion" />
                            </div>
                        </div>
                        <span>•</span>
                        <p>{{ publicacion.tiempo }}</p>

                    </div>
                    <div class="flex gap-1 items-center justify-end">
                        <button class="flex justify-end text-2xl pr-4 md:p-2.5 text-white cursor-pointer">...</button>
                    </div>
                </div>
                <img :src="publicacion.ft" class="md:border rounded-[5px] border-[#262626]" />
                <div class="flex w-full">
                    <div class="flex w-1/2">
                        <div class="flex gap-4 p-3">
                            <div class="flex justify-start gap-1 cursor-pointer">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                                    class="w-6 h-6 shrink-0 text-white transition-transform duration-300 hover:scale-110">
                                    <title>Notificaciones</title>
                                    <path
                                        d="M16.792 3.904A4.989 4.989 0 0 1 21.5 9.122c0 3.072-2.652 4.959-5.197 7.222-2.512 2.243-3.865 3.469-4.303 3.752-.477-.309-2.143-1.823-4.303-3.752C5.141 14.072 2.5 12.167 2.5 9.122a4.989 4.989 0 0 1 4.708-5.218 4.21 4.21 0 0 1 3.675 1.941c.84 1.175.98 1.763 1.12 1.763s.278-.588 1.11-1.766a4.17 4.17 0 0 1 3.679-1.938m0-2a6.04 6.04 0 0 0-4.797 2.127 6.052 6.052 0 0 0-4.787-2.127A6.985 6.985 0 0 0 .5 9.122c0 3.61 2.55 5.827 5.015 7.97.283.246.569.494.853.747l1.027.918a44.998 44.998 0 0 0 3.518 3.018 2 2 0 0 0 2.174 0 45.263 45.263 0 0 0 3.626-3.115l.922-.824c.293-.26.59-.519.885-.774 2.334-2.025 4.98-4.32 4.98-7.94a6.985 6.985 0 0 0-6.708-7.218Z">
                                    </path>
                                </svg>
                                <p class="text-white">{{ publicacion.likes }}</p>
                            </div>
                            <div class="flex justify-start gap-1 cursor-pointer">
                                <svg aria-label="Comentar"
                                    class="w-6 h-6 shrink-0 text-white transition-transform duration-300 hover:scale-110"
                                    fill="currentColor" height="24" role="img" viewBox="0 0 24 24" width="24">
                                    <title>Comentar</title>
                                    <path d="M20.656 17.008a9.993 9.993 0 1 0-3.59 3.615L22 22Z" fill="none"
                                        stroke="currentColor" stroke-linejoin="round" stroke-width="2"></path>
                                </svg>
                                <p class="text-white">{{ publicacion.coments }}</p>
                            </div>
                            <div class="flex justify-start gap-1 cursor-pointer">
                                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor"
                                    class="w-6 h-6 shrink-0 text-white transition-transform duration-300 hover:scale-110">
                                    <title>Mensajes</title>
                                    <path
                                        d="M13.973 20.046 21.77 6.928C22.8 5.195 21.55 3 19.535 3H4.466C2.138 3 .984 5.825 2.646 7.456l4.842 4.752 1.723 7.121c.548 2.266 3.571 2.721 4.762.717Z"
                                        fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2">
                                    </path>
                                    <line fill="none" stroke="currentColor" stroke-linecap="round"
                                        stroke-linejoin="round" stroke-width="2" x1="7.488" x2="15.515" y1="12.208"
                                        y2="7.641"></line>
                                </svg>
                            </div>
                        </div>
                    </div>
                    <div class="w-1/2">
                        <div class="flex justify-end gap-1 items-center p-3 cursor-pointer">
                            <svg aria-label="Guardar"
                                class="w-6 h-6 shrink-0 text-white transition-transform duration-300 hover:scale-110"
                                fill="currentColor" height="24" role="img" viewBox="0 0 24 24" width="24">
                                <title>Guardar</title>
                                <polygon fill="none" points="20 21 12 13.44 4 21 4 3 20 3 20 21" stroke="currentColor"
                                    stroke-linecap="round" stroke-linejoin="round" stroke-width="2"></polygon>
                            </svg>
                        </div>
                    </div>

                </div>
                <div class="group pl-3 pr-3 md:p-0">
                    <p :class="{ 'line-clamp-2': !publicacion.expandido }" class=" font-normal text-white">
                        <span class="font-bold cursor-pointer">{{ publicacion.usuario }}</span> {{
                            publicacion.descripcion
                        }}


                    </p>
                    <div class="absolute flex items-center justify-center cursor-pointer invisible 
              group-hover:visible opacity-100  delay-800 w-3/5">
                        <Preperfil :item="publicacion" />
                    </div>
                </div>
                <button v-if="!publicacion.expandido && publicacion.descripcion.length > 100"
                    @click="publicacion.expandido = true"
                    class="flex text-gray-400 hover:text-gray-200 ml-1 cursor-pointer justify-start pl-3 md:pl-0">
                    más
                </button>
            </li>

        </ul>

    </div>
</template>
