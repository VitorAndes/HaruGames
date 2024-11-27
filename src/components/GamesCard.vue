<script setup lang="ts">
import { ref } from 'vue';

interface Games {
    game_img: string;
    game_title: string;
    game_description: string;
}

const games = ref<Games[]>([
    {
        game_img: '/assets/game_mass.svg',
        game_title: '',
        game_description: ''
    },
    {
        game_img: '/assets/game_henn.svg',
        game_title: '',
        game_description: ''
    },
    {
        game_img: '/assets/game_desi.svg',
        game_title: '',
        game_description: ''
    },
    {
        game_img: '/assets/game_vent.svg',
        game_title: '',
        game_description: ''
    }
]); 
</script>

<template>
    <div id="games_container">
        <div v-motion-fade v-for="game in games" :key="game.game_title" class="game_card">
            <img :src="game.game_img" alt="imagem do jogo" class="game_img">
            <h2 class="game_title">{{ game.game_title }}</h2>
            <p class="game_description">{{ game.game_description }}</p>
        </div>
    </div>
</template>

<style lang="less">
@import '../variables.less';

#games_container {
    display: flex;
    flex-wrap: wrap;
    gap: 6px;

    .game_card {
        border-radius: @border_radius;
        height: 230px;
        width: 192px;
    }
}
</style>