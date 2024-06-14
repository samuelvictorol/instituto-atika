<template>
    <div class="loading animate__animated animate__fadeIn animate__slow">
        <q-spinner-hourglass
        color="primary"
        size="4em"
    />
    </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.loading {
    position: fixed;
    z-index: 9999!important;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 53, 61, 0.732);
    backdrop-filter: blur(5px);
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>