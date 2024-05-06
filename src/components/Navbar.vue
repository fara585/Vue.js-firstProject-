<template>
    <nav class="nav">
        <div class="container">
            <div class="nav__content">

                <div class="hamburger">
                    <span></span>
                    <span></span>
                    <span></span>
                </div>

                <div class="nav__content-block">
                    <img src="../assets/img/nav__title.svg" alt="">
                    <div class="nav__block-txt">
                        <p>В партнерстве с</p>
                        <img src="../assets/img/logo-bottom.png" alt="">
                    </div>
                </div>

                <h3 class="nav__content-title">Проведено торгов: <span>{{ sold }}</span> </h3>

                <form class="nav__content-frm">
                    <div class="nav__frm-search">
                        <img src="../assets/img/search.svg" alt="">
                        <input type="search" placeholder="Поиск по лотам" v-model="search">
                    </div>
                    <button class="nav__frm-btm">Личный кабинет</button>
                </form>
                
            </div>
        </div>
    </nav>
    <Header />
</template>

<script>
import Header from '@/components/Header.vue'


export default {
    components: {
        Header
    },
    data() {
        return {
            sold: '12 345',
            search: '',
        }
    },
}
</script>

<style>
.nav {
    border: 1px solid #1C426D
}

.nav__content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 25px 0;
}

.hamburger {
    position: relative;
    width: 35px;
    height: 18px;
    cursor: pointer;
}

.hamburger span {
    position: absolute;
    width: 100%;
    height: 2px;
    background: #163C66;
}

.hamburger span:nth-child(3) {
    position: absolute;
    bottom: 0;
}

.hamburger span:nth-child(2) {
    position: absolute;
    top: 8px;
}

.nav__content-block {
    display: flex;
    flex-direction: column;
    gap: 14px;
}

.nav__block-txt {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
}

.nav__block-txt p {
    font-size: 12px;
    color: #21212666;

}

.nav__content-title {
    color: #8C9091;
    font-size: 14px;
    left: 13.4px;
}

.nav__content-title span {
    color: #163C66;
    font-family: "GothamProBold";
    font-size: 16px;
}

.nav__content-frm {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
}

.nav__frm-search {
    display: flex;
    align-items: center;
    gap: 15px;
    padding: 13px 20px;
    border: 1px solid #1C426D33;
    border-radius: 6px;
}

.nav__content-frm input {
    outline: none;
    border: none;
    color: #8C9091;
}

.nav__frm-btm {
    border: none;
    outline: none;
    background: #1C426D;
    color: white;
    left: 19.2px;
    text-align: center;
    padding: 14px 22.5px;
    border-radius: 6px;
    cursor: pointer;
}
</style>