<template>
    <header class="Header">
        <div class="logo">
            <a href="#"><img :src="require('@/assets/images/firstlogo.png')" alt=""></a>
        </div>
        <nav>
            <ul class="menu">
                <li class="menu_link"><a href="#">Главная</a></li>
                <li class="menu_link"><a href="#">Услуги</a></li>
                <li class="menu_link"><a href="#">Работы</a></li>
                <li class="menu_link"><a href="#">О нас</a></li>
                <li class="menu_link"><a href="#">Связаться</a></li>
            </ul>
        </nav>
        <div class="links">
            <div class="social_links"></div>
            <div class="social_links"></div>
            <div class="social_links"></div>
        </div>
    </header>
</template>

<script>
export default{
    name: "Header",
    props:{

    },
    data(){
        return{}
    },
    computed:{}
}
</script>

<style>
.Header{
    display: flex;
    justify-content: space-between;
}
ul{
    display: flex;
    justify-content: space-between;
}
.links{
    display: flex;
    justify-content: space-between;
}
.menu_link{
    margin-left: 54px;
}
.social_links{
    width: 70px;
    height: 70px;
    background-color: white;
    margin-left: 11px;
}
</style>