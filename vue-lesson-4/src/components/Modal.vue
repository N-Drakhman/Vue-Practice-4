<script setup></script>

<template>
    <div class="overlay">
        <div class="modal-dialog">
<slot></slot>

        </div>
    </div>
</template>

<style scoped>
.overlay{
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.1);
    position: fixed;
    display: flex;
    align-items: center;
    justify-content: center;
    top: 0;
    left: 0;
}

.modal-dialog{
    width: 40%;
    height: 50%;
    background-color: #fff;
    border-radius: 15px;
    padding: 15px;
    color: black
}
</style>