<script setup>
import { computed, ref } from 'vue';

const props = defineProps({
  items: {
    type: Array,
    required: true,
    default: () => []
  }
});

/**
 * CONFIGURACIÓN
 */
const visible = 6;          // elementos visibles
const paso = 4;             // cuántos avanza

const cardWidth = 80 + (props.items.length)/2;       // ancho aproximado del item 

/**
 * ESTADO
 */
const inicio = ref(0);
const animando = ref(false);

/**
 * TRANSFORM CALCULADO
 */
const offset = computed(() => {
  return -(inicio.value * cardWidth);
});

/**
 * NAVEGACIÓN
 */
const proximo = () => {
  if (animando.value) return;

  if (inicio.value + visible < props.items.length) {
    animando.value = true;
    inicio.value = Math.min(
      inicio.value + paso,
      props.items.length - visible
    );
  }
};

const atras = () => {
  if (animando.value) return;

  if (inicio.value > 0) {
    animando.value = true;
    inicio.value = Math.max(0, inicio.value - paso);
  }
};

const finAnimacion = () => {
  animando.value = false;
};
</script>

<template>
  <div class="flex items-center relative">

    <!-- BOTÓN ATRÁS -->
    <div
      @click="atras"
      class="absolute left-0 z-10 flex items-center justify-center cursor-pointer
             hover:scale-110 transition-transform"
      :class="{ 'pointer-events-none opacity-0': animando || inicio === 0 }"
    >
      <img src="./icons/back.png" class="h-6" />
    </div>

    <!-- CONTENEDOR -->
    <div class="overflow-hidden flex-1 mx-10">

      <ul
        @transitionend="finAnimacion"
        class="flex gap-4 items-center
               transition-transform duration-500 ease-out
               will-change-transform select-none"
        :style="{ transform: `translateX(${offset}px)` }"
      >
        <li
          v-for="perfil in props.items"
          :key="perfil.id"
          class="flex flex-col items-center cursor-pointer flex-shrink-0"
        >
          <div class="rounded-full p-0.75 bg-gradient-to-tr from-[#ffec00] via-[#ff3041] to-[#ff00ee]">
            <div class="rounded-full bg-[#181818] p-1">
              <img
                :src="perfil.ftperfil"
                class="w-17 h-17 object-cover rounded-full"
              />
            </div>
          </div>

          <p class="font-normal text-white text-xs mt-1">
            {{ perfil.nombre }}
          </p>
        </li>
      </ul>

    </div>

    <!-- BOTÓN SIGUIENTE -->
    <div
      @click="proximo"
      class="absolute right-0 z-10 flex items-center justify-center cursor-pointer
             hover:scale-110 transition-transform"
      :class="{
        'pointer-events-none opacity-0':
          animando || inicio + visible >= props.items.length
      }"
    >
      <img src="./icons/proximo.png" class="h-6" />
    </div>

  </div>
</template>
