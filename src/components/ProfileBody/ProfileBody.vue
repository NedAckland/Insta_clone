<template>
  <div class="body-wrapper">
    <div class="body">
      <div class="body__nav">
        <span>POSTS</span>
        <span>IGTV</span>
        <span>SAVED</span>
        <span>TAGGED</span>
      </div>
      <Posts />

    </div>
  </div>
</template>

<script>
import Posts from "@/components/ProfileBody/Posts";
export default {
  name: "ProfileBody",
  components: {
    Posts,
  }
}
</script>


<style scoped lang="scss">
.body-wrapper {
  margin: 0 1.5rem;
  border-top: 1px solid #cecece;
  .body {
    &__nav {
      cursor: pointer;
      font-weight: bolder;
      font-size: small;
      color: #8d8d8d;
      height: 50px;
      max-width: 400px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
}
</style>