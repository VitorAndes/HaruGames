<script setup lang="ts">
import GameHub from './components/GameHub.vue';
import ProfileCard from './components/ProfileCard.vue';
</script>

<template>
  <div id="body">
    <div id="container">
      <ProfileCard />
      <GameHub />
    </div>
  </div>
</template>

<style lang="less">
@import '/src/variables.less';

#body {
  display: flex;
  justify-items: center;
  min-height: 100vh;
  padding: 12px;

  #container {
    display: flex;
    flex-direction: column;
    gap: 12px;
    width: 100%;

    @media (min-width: 768px) {
      width: 100%;
      padding: 2rem;
    }

    @media (min-width: 1380px) {
      width: max(1300px);
      padding: 2rem;
    }
  }
}
</style>
