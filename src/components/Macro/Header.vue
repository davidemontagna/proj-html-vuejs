<template>
    <header>
        <div class="bg-top-header d-flex align-items-center">
            <top-nav />
        </div>
        <div class="container my-4">
            <div class="row">
                <div class="col-12 col-sm-6 col-lg-3">
                    <div class="dm-logo">
                        <img src="../../assets/img/logos/logo-default-slim.png" alt="">
                    </div>
                </div>
            </div>
        </div>
        <div class="dm-bottom-nav d-flex align-items-center">
            <bottom-nav />
        </div>
        
        
    </header>
</template>

<script>
import TopNav from "../commons/TopNav.vue";
import BottomNav from "../commons/BottomNav.vue";

export default {
    name: 'Header',
    components: {
        TopNav,
        BottomNav
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.bg-top-header{
    background-color: $bg-color-6;
    height: 50px;    
    width: 100vw;
}

.dm-logo{
    img{
        height: 60px;        
    }
}

.dm-bottom-nav{
    padding: 10px;
    border-top: 1px solid $border-color-3;
}
</style>