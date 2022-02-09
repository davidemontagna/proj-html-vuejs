<template>
    <main>
        <div class="dm-top-grid">
            <div class="container">
                <div class="row w-100">
                    <div class="col-12 col-sm-6 col-lg-3 w-100 d-flex justify-content-between flex-wrap">
                        <labels-grid />
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row w-100">
                <div class="col-12 col-sm-6 col-lg-3 w-100">
                    <all-posts />
                </div>
            </div>
        </div>
        <div class="my-5 dm-buttons-row d-flex align-items-center">
            <div class="container">
                <div class="row w-100">
                    <div class="col-12 col-sm-6 w-100">
                        <buttons />
                    </div>
                </div>
            </div>
        </div>
        <div class="container">
            <div class="row w-100">
                <div class="col-12 col-sm-6 col-lg-3 w-100 clearfix">
                    <div class="float-start dm-posts-section">
                        <posts-big />
                    </div>
                    <div class="float-end dm-socials-section">
                        <socials />
                    </div>
                    
                    
                </div>
            </div>
        </div>
        
    </main>
</template>

<script>
import LabelsGrid from "../commons/LabelsGrid.vue";
import AllPosts from "../commons/AllPosts.vue";
import Buttons from "../commons/Buttons.vue";
import PostsBig from "../commons/PostsBig.vue";
import Socials from "../commons/Socials.vue";

export default {
    name: 'Main',
    components:{
        LabelsGrid,
        AllPosts,
        Buttons,
        PostsBig,
        Socials
    },
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-top-grid{
    background-color: $bg-color-2;
    padding: 30px;
}

.dm-buttons-row{
    height: 140px;
    background-color: $bg-color-5;
}

.dm-posts-section{
    width: 65%;
}

.dm-socials-section{
    widows: 30%;
}
</style>