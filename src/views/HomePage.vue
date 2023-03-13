<template>
  <div class="welcome">
    <h1>
      Welcome <br>
      to <br>
      Black Jack
    </h1>
    <router-link class="welcome-link" to="game">
      <span>Start</span>
      <span class="welcome-link-arrow">></span>
    </router-link>
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

.welcome-link {
  height: 60px;
    background-color: var(--main-color);
    display: block;
    color: var(--secondary-color);
    text-decoration: none;
    font-size: 40px;
    line-height: 60px;
    font-weight: 700;
    text-transform: uppercase;
    padding: 0 20px;

    &:hover {
      .welcome-link-arrow {
        &::before {
          left: 20px;
          transition: left var(--main-transition);
        }

        &::after {
          left: 40px;
          transition: left var(--main-transition);
        }
      }
    }
}

.welcome-link-arrow {
  position: relative;

  &::before,
  &::after {
    content: '>';
    display: inline-block;
    position: absolute;
    left: 0;
    transition: left var(--main-transition);
  }
}
</style>
