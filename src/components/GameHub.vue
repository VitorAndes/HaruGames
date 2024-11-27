<script setup lang="ts">
import GamesCard from './GamesCard.vue'
</script>

<template>
  <div id="Container_gameHub">
    <header class="gameHub_header">
      <h1>Steam</h1>
    </header>
    <div class="gamehub_games">
      <GamesCard />
    </div>
  </div>
</template>

<style lang="less">
@import '../variables.less';

#Container_gameHub {
  display: flex;
  flex-direction: column;
  gap: 16px;

  .gameHub_header {
    height: 50px;
    width: 100%;
    border-radius: @border_radius;
    .background_glass();
    display: flex;
    align-items: center;
    padding: 8px;

    h1 {
      .format_title();
    }
  }

}
</style>
