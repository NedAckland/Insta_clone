<template>
  <div v-if="isSelected">Saved</div>
</template>

<script>
export default {
  name: "Saved",
  props: {
    isSelected: Boolean,
  }
}
</script>

<style scoped>

</style>