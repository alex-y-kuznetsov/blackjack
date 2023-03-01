<template>
  <div class="welcome">
    <h1>
      Welcome <br>
      to <br>
      Black Jack
    </h1>
    <router-link class="welcome-link" to="game">Start Game</router-link>
  </div>
</template>

<script>
export default {
  name: 'HomePage'
}
</script>

<style lang="less" scoped>
.welcome {
  h1 {
    font-size: 80px;
    line-height: 88px;
    text-transform: uppercase;
    font-weight: 900;
  }
}
</style>
