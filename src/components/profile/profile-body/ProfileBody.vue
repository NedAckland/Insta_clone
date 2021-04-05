<template>
  <div class="body-wrapper">
    <div class="body">
      <div class="body__nav">
        <div :key="page.id" v-for="page in pages">
          <span :class="{selected: page.selected}" @click="select(page.id)">{{page.name.toLocaleUpperCase()}}</span>
        </div>
      </div>
      <Posts :isSelected="currentPage(0)" />
      <IGTV :isSelected="currentPage(1)" />
      <Saved :isSelected="currentPage(2)" />
      <Tagged :isSelected="currentPage(3)" />
    </div>
  </div>
</template>

<script>

import Posts from "@/components/profile/profile-body/Posts";
import IGTV from "@/components/profile/profile-body/IGTV";
import Saved from "@/components/profile/profile-body/Saved";
import Tagged from "@/components/profile/profile-body/Tagged";

export default {
  name: "ProfileBody",
  components: {
    Posts,
    IGTV,
    Saved,
    Tagged
  },
  data() {
    return {
      pages: [
        { name: 'Posts', selected: true, id: 0 },
        { name: 'IGTV', selected: false, id: 1 },
        { name: 'Saved', selected: false, id: 2 },
        { name: 'Tagged', selected: false, id: 3 },
      ]
    }
  },
  methods: {
    select(i) {
      this.pages.map(page => page.selected = false)
      this.pages[i].selected = true
    },
    currentPage(i){
      return this.pages[i].selected
    }
  },
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
      max-width: 400px;
      margin: 20px auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
  }
  .selected {
    color: black;
  }
}
</style>