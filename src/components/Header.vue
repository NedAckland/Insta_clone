<template>
  <div class="header--underline">
    <div class="header--wrapper">
      <div class="logo">
        <img class="logo__image" src="https://1000logos.net/wp-content/uploads/2017/02/Instagram-Logo.png" alt="">
      </div>
      <input class="header__search-bar">
      <div class="avatar">
        <img @click="setPopupVisible" class="avatar__picture" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUf9QPA3pe7BY91OIKO_4xqJfLRsPWJyHDRQ&usqp=CAU" alt="">
					<Dropdown :isVisible="popupVisible" />
      </div>
    </div>
  </div>
</template>

<script>
import Dropdown from './dropdown/Dropdown'

export default {
	name: "Header",
	components: {
		Dropdown,
	},
	data() {
		return {
			popupVisible: true,
		}
	},
	methods: {
		setPopupVisible() {
			this.popupVisible = !this.popupVisible
		}
	},

}
</script>

<style scoped lang="scss">
.popup--wrapepr {
	position: absolute;
}
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
      border: 1px solid #c4c4c4;
      &:hover{
        border: 1px solid #b1b1b1;
      }
    }
  }
  .avatar {
    cursor: pointer;
    width: 30px;
    height: 30px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 50%;
    border: 1.5px solid black;
    
    &__picture {
      width: 90%;
      text-align: center;
      border-radius: 50%;
    }
  }
}
</style>