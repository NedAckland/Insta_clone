<template>
  <div class="profile--wrapper">
    <div class="avatar">
      <img class="avatar__picture" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUf9QPA3pe7BY91OIKO_4xqJfLRsPWJyHDRQ&usqp=CAU" alt="">
    </div>
    <div class="user">
      <div class="user__display-name">nedackland</div>
        <div class="user__stats">
          <span><strong>20</strong> post</span>
          <span><strong>20</strong> followers</span>
          <span><strong>20</strong> following</span>
        </div>
      <div class="user__name">Ned Baring</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProfileTop"
}
</script>

<style scoped lang="scss">
.profile--wrapper {
  display: flex;
  justify-content: space-evenly;
  margin: 35px auto;
  max-width: 800px;
  .avatar {
    width: 150px;
    &__picture{
      z-index: -1;
      border-radius: 50%;
      width: 100%;
     }
  }
  .user {
    margin: 0 30px;
    &__display-name {
      font-size: x-large;
      margin-bottom: 30px;
    }
    &__stats {
      display: flex;
      justify-content: space-between;
      gap: 50px;
      margin-bottom: 30px;
    }
    &__name {

      font-weight: bolder;
    }
  }
}
</style>