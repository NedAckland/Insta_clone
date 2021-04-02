<template>
  <div class="header--underline">
    <div class="header--wrapper">
      <div class="logo">
        <img class="logo__image" src="https://1000logos.net/wp-content/uploads/2017/02/Instagram-Logo.png" alt="">
      </div>
      <input class="header__search-bar">
      <div>here</div>
    </div>
  </div>
</template>

<script>
export default {
name: "Header"
}
</script>

<style scoped lang="scss">

.header--underline {
    width: 100vw;
    border-bottom: 1px solid #cecece;
}
.header--wrapper{
    max-width: 800px;
    height: 3.3rem;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  .logo {
    width: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
    &__image {
      width: 100%;
    }
  }
  .header{
    &__search-bar{
      width: 30%;
      height: 30px;
      border-radius: 5px;
      background-color: #fff;
      border: 1px solid #8d8d8d;
      &:hover{
        border: 2px solid #2100b3;
      }
    }
  }
}
</style>