<template>
  <div v-if="isSelected">Tagged</div>
</template>

<script>
export default {
  name: "Tagged",
  props: {
    isSelected: Boolean,
  }
}
</script>

<style scoped>

</style>