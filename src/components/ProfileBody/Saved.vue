<template>
  <div v-if="isSelected">
    <p class="info-text">Only you can see what you've saved</p>
    <div class="posts-wrapper">
      <div v-bind:key="post" v-for="post in savedPosts">
        <div class="post"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Saved",
  props: {
    isSelected: Boolean,
  },
  data() {
    return {
      savedPosts: [1, 2, 3, 4]
    }
  },
}
</script>

<style scoped lang="scss">
.posts-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
  overflow-x: hidden;
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
.info-text {
  text-align: center;
  margin: 10px;
  color: #8d8d8d;
  font-size: small;
}
</style>