<script setup lang="ts">
import { ref } from 'vue';

interface Games {
    game_img: string;
    game_title: string;
}

const games = ref<Games[]>([
    {
        game_img: 'https://www.minecraft.net/content/dam/minecraftnet/games/minecraft/key-art/Homepage_Discover-our-games_MC-Vanilla-KeyArt_864x864.jpg',
        game_title: 'Minecraft'
    },
    {
        game_img: 'https://assetsio.gnwcdn.com/co49wj.jpg?width=1200&height=1200&fit=bounds&quality=70&format=jpg&auto=webp',
        game_title: 'LOL'
    },
    {
        game_img: 'https://www.adrenaline.com.br/wp-content/uploads/2023/05/valorant-cover.jpg',
        game_title: 'Valorant'
    },
    {
        game_img: 'https://cdn2.steamgriddb.com/grid/d18c832e8c956b4ef8b92862e6bf470d.png',
        game_title: 'Hollow knight'
    },
    {
        game_img: 'https://sm.ign.com/ign_br/cover/c/celeste/celeste_y4wf.jpg',
        game_title: 'Celeste'
    },
    {
        game_img: 'https://upload.wikimedia.org/wikipedia/pt/1/1b/Little_Nightmares_capa_do_jogo.jpg',
        game_title: 'Little nightmares'
    }
]); 
</script>

<template>
    <div id="games_container">
        <div v-motion-fade v-for="game in games" :key="game.game_title" class="game_card">
            <img class="game__img" :src="game.game_img">
            <div class="card-label__container">
                <div class="card-label__content">
                    <p>{{ game.game_title }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="less">
@import '../variables.less';

#games_container {
    display: flex;
    padding: 10px;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px 0px;

    .game_card {
        position: relative;
        border: 3px solid #3E4357;
        border-radius: 10px;
        .backgroundCard_glass();

        width: 230px;
        height: 330px;

        display: flex;
        overflow: hidden;

        p {
            .format_description();
        }

        .game__img {
            min-width: 100%;
            min-height: 100%;

            transition: transform .8s;

            &:hover {
                transform: scale(1.1);
            }
        }

        .card-label__container {
            position: absolute;
            bottom: 30px;
            right: 0;

            .card-label__content {
                display: flex;
                align-items: center;
                justify-content: center;
                background-color: #0d0d0dc1;

                color: white;
                font-size: 12px;
                font-weight: bold;

                height: 40px;
                padding: 0px 50px;
            }

        }

    }
}
</style>