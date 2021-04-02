<template>
  <div class="posts-wrapper">
    <div v-bind:key="post" v-for="post in posts">
      <div class="post">

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Posts",
  data() {
    return {
      posts: [1, 2, 3, 4, 5, 6]
    }
  }

}
</script>

<style scoped lang="scss">
.posts-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  max-width: 900px;
  gap: 20px;
  .post {
    width: 100%;
    height: 300px;
    max-width: 350px;
    max-height: 350px;
    background-color: #e2e2e2;
  }
}
</style>