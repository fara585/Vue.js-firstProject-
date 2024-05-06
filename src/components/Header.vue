<template>
    <header class="header">
        <h1 class="header__content-title">{{ mainTitle }}</h1>
        <div class="header__content"></div>
    </header>
</template>

<script>
export default {
    data() {
        return {
            mainTitle: 'Автомобильный аукцион SD-assist.ru'
        }
    },
}
</script>

<style>
.header {
    display: flex;
    flex-direction: column;
    gap: 75px;
    padding: 73px 0 97px;
}

.header__content-title {
    align-self: center;
    width: 680px;
    text-align: center;
    font-size: 62px;
    color: #000000;
    font-family: "GothamProBold";
    line-height: 68.2px;
}

.header__content {
    width: 100%;
    height: 80vh;
    background: url(../assets/img/header__bg.png) no-repeat center/cover;
}
</style>