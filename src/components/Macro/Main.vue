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
        
    </main>
</template>

<script>
import LabelsGrid from "../commons/LabelsGrid.vue"
import AllPosts from "../commons/AllPosts.vue"

export default {
    name: 'Main',
    components:{
        LabelsGrid,
        AllPosts
    },
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-top-grid{
    background-color: $bg-color-2;
    padding: 30px;
}
</style>