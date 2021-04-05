<template>
    <div v-show="isVisible" class="popup">
        basic dropdown
    </div>
</template>

<script>
export default {
    name: "Dropdown",
    props: {
        isVisible: Boolean,
    },
}
</script>

<style scoped lang="scss">
.popup {
    width: 200px;
    height: 150px;
    position: absolute;
    background-color: rgb(255, 255, 255);
    top: 52px;
    margin-right: 107px;
    z-index: 500;
    padding: 1.125em 1.5em;
    border-radius: 0.5rem;
    box-shadow:	0 0.125rem 0.5rem rgba(0, 0, 0, .3), 0 0.0625rem 0.125rem rgba(0, 0, 0, .2);
    &:before {
        content: '';
        position: absolute;
        width: 0;
        height: 0;
        bottom: 100%;
        left: 9em; 
        border: .6rem solid transparent;
        border-top: none;
        border-bottom-color: rgb(255, 255, 255);
        filter: drop-shadow(0 -0.0625rem 0.0625rem rgba(0, 0, 0, .1));
    }
}
</style>