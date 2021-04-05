<template>
  <div class="igtv-wrapper" v-if="isSelected">
    <div class="content">
      <h2 class="content__header">Upload a Video</h2>
      <p class="content__para">Videos must be between 1 and 60 minutes long</p>
      <button>Upload</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "IGTV",
  props: {
    isSelected: Boolean,
  }
}
</script>

<style scoped lang="scss">
.igtv-wrapper {
  display: flex;
  justify-content: center;
  align-self: center;
  margin: 100px 0;
  .content {
    max-width: 300px;
    display: grid;
    justify-content: center;
    align-self: center;
    text-align: center;
    gap: 30px;
    &__header {
      font-size: xx-large;
      font-weight: 500;
    }
    &__para {
      font-size: small;
    }
  }
  button{
    cursor: pointer;
    width: 30%;
    height: 2em;
    border-radius: 7px;
    margin: 0 auto;
    background-color: #0088ff;
    border: 1px solid #0088ff;
    color: white;
    font-weight: bold;
  }
}
</style>