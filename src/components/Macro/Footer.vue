<template>
    <footer>
        <div class="dm-foot-top">
            <div class="container position-relative">
                <div class="row w-100">
                    <div class="col-12 col-sm-6 col-lg-3 w-100">
                        
                        <div >
                            <div class="d-inline" id="triangle-up"></div>
                            <span class="dm-get-in-touch">Get in Touch</span>
                        </div>
                        <foot-top />
                    </div>
                </div>
            </div>            
        </div>
        <div class="dm-foot-boottom position-relative">
            <div class="container position-relative">
                <div class="row w-100">
                    <div class="col-12 col-sm-6 col-lg-3 w-100">
                        <foot-bottom />
                    </div>
                </div>
            </div>
            <div class="dm-arrow-up text-center d-flex justify-content-center align-items-center">
                <i class="fa-solid fa-chevron-up"></i>
            </div> 
        </div>
        
    </footer>
</template>

<script>
import FootTop from "../commons/FootTop.vue"
import FootBottom from '../commons/FootBottom.vue'

export default {
    name: 'Footer',
    components:{
        FootTop,
        FootBottom
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-foot-top{
    background-color: $bg-color-7;
}

.dm-get-in-touch{
    background-color: $bg-color-5;
    padding: 10px 15px;
    color: $font-color-1!important;
    font-family: $secondary-font;
    font-size: 14px;
}

#triangle-up {
    position: absolute;
    top: -9px;
    left: 2px;
    width: 0;
    height: 0;
    border-left: 10px solid transparent;
    border-right: 0px solid transparent;
    border-bottom: 9px solid $bg-color-6;
}

.dm-foot-boottom{
    background-color: $bg-color-8;
}

.dm-arrow-up{
    position: absolute;
    right: 15px;
    bottom: 0;   
    width: 40px;
    height: 40px;
    background-color: $bg-color-7;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    color: $font-color-1;
}
</style>