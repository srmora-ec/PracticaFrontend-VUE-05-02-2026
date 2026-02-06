<script setup>
const props = defineProps({
    item: {
        type: Object,
        required: true
    }
});
</script>

<template>
    <div class="bg-[#212328] rounded-2xl w-full cursor-default">
        <div class=" p-5">
            <div class="flex">
                <div class="rounded-full bg-[#2b3036] p-1">
                    <img :src="item.ftperfil" class="w-17 h-17 object-cover rounded-full" />
                </div>
                <div class="pl-5">
                    <p class="font-bold text-white">{{ item.usuario }}</p>
                    <p class="text-xs">joseAlvarezMora</p>
                </div>
            </div>
            <div class="flex justify-between">
                <div class="flex flex-col items-center pt-3 pb-3">
                    <div class="font-bold text-white text-sm">1500</div>
                    <div class="text-white text-sm">Publicaciones</div>
                </div>
                <div class="flex flex-col items-center pt-3 pb-3">
                    <div class="font-bold text-white text-sm">523 mil</div>
                    <div class="text-white text-sm">Seguidores</div>
                </div>
                <div class="flex flex-col items-center pt-3 pb-3">
                    <div class="font-bold text-white text-sm">1500</div>
                    <div class="text-white text-sm">Seguidos</div>
                </div>
            </div>

        </div>
        <div class="flex gap-0.5">
            <div class="flex flex-col items-center pb-3">
                <img src="https://pbs.twimg.com/media/G8CRfvebAAA1x7n?format=jpg&name=4096x4096" class="w-32 h-32 object-cover"/>
            </div>
            <div class="flex flex-col items-center pb-3">
                <img src="https://pbs.twimg.com/media/G7eL3O4bQAABZ2V?format=jpg&name=4096x4096"  class="w-32 h-32 object-cover"/>
            </div>
            <div class="flex flex-col items-center pb-3">
                <img src="https://pbs.twimg.com/media/G66JB6FakAAxztD?format=jpg&name=4096x4096"  class="w-32 h-32 object-cover"/>
            </div>
        </div>
     <div class="flex gap-1 pl-5 pr-5 pb-5 w-full">
    <button class="flex-1 flex justify-center text-white bg-[#333fc3] py-2 rounded font-normal text-xs items-center cursor-pointer hover:bg-[#4150f7]">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" class="w-4 h-4 shrink-0 mr-1">
            <path d="M13.973 20.046 21.77 6.928C22.8 5.195 21.55 3 19.535 3H4.466C2.138 3 .984 5.825 2.646 7.456l4.842 4.752 1.723 7.121c.548 2.266 3.571 2.721 4.762.717Z" fill="none" stroke="currentColor" stroke-linejoin="round" stroke-width="2"></path>
            <line fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" x1="7.488" x2="15.515" y1="12.208" y2="7.641"></line>
        </svg>
        <span>Enviar mensaje</span>
    </button>

    <button class="flex-1 flex justify-center text-white bg-[#0d0f10] py-2 rounded font-normal text-xs items-center cursor-pointer hover:bg-[#363c44]">
        Siguiendo
    </button>
</div>
    </div>

</template>