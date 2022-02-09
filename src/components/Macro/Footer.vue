<template>
    <footer>
        <div class="dm-foot-top">
            <div class="container">
                <div class="row w-100">
                    <div class="col-12 col-sm-6 col-lg-3 w-100">
                        <foot-top />
                    </div>
                </div>
            </div>            
        </div>
        
    </footer>
</template>

<script>
import FootTop from "../commons/FootTop.vue"

export default {
    name: 'Footer',
    components:{
        FootTop
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-foot-top{
    background-color: $bg-color-7;
}
</style>