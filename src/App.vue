<template>
  <div class="container">
    <header class="header">
      <BJHeader />
    </header>
    <main class="main">
      <router-view/>
    </main>
    <footer class="footer">
      <BJFooter />
    </footer>
  </div>
</template>

<script>
import BJHeader from '@/components/BJHeader.vue'
import BJFooter from '@/components/BJFooter.vue'

export default {
  name: 'App',
  components: {
    BJHeader,
    BJFooter
  }
}
</script>

<style lang="less">
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,400;0,700;0,900;1,400&display=swap');

:root {
  //colors
  --main-color: #FFFFFF;
  --secondary-color: #16123F;
  --bg-gradient: linear-gradient(90deg, #ABD699, #75C9B7);
}

html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
}

#app {
  height: 100%;
  font-family: 'Roboto', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: var(--main-color);
  background: var(--bg-gradient);
}

.header {
  padding: 20px 0
}

.main {
  flex: 1 1 0;
}

.footer {
  padding: 20px 0;
}

.container {
    max-width: 800px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    flex-direction: column;
    height: 100%;
}
</style>
