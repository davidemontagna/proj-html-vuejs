<template>
    <header>
        <div class="bg-top-header d-flex align-items-center">
            <top-nav />
        </div>
        <div class="container my-4">
            <div class="row">
                <div class="col">
                    <div class="dm-logo">
                        <img src="../assets/img/logos/logo-default-slim.png" alt="">
                    </div>
                </div>
            </div>
        </div>
        
        
    </header>
</template>

<script>
import TopNav from "./commons/TopNav.vue"

export default {
    name: 'Header',
    components: {
        TopNav
    }
}
</script>

<style lang="scss">
.bg-top-header{
    background-color: #0088cc;
    height: 50px;    
    width: 100vw;
}

.dm-logo{
    img{
        height: 60px;
        
    }
}
</style>