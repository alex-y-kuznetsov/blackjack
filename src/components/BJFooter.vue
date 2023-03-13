<template>
  <div class="footer-cover">
    <div class="footer-buttons">
      <button class="footer-info">?</button>
    </div>
    <div class="footer-copiright">{{  getYear() }}</div>
  </div>
</template>

<script>
export default {
  name: 'BJFooter',
  methods: {
    getYear () {
      const today = new Date()
      return today.getFullYear()
    }
  }
}
</script>

<style lang="less" scoped>
  .footer-cover {
    display: flex;
    justify-content: space-between;
  }

  .footer-info {
    border: 2px solid var(--main-color);
    color: var(--main-color);
    background-color: transparent;
    font-size: 20px;
    font-weight: bold;
    cursor: pointer;
    transition: all var(--main-transition);

    &:hover {
      background-color: var(--main-color);
      color: var(--secondary-color);
      transition: all var(--main-transition);
    }
  }

  .footer-copiright {
    display: flex;
    align-items: center;
    font-weight: 700;
  }
</style>
