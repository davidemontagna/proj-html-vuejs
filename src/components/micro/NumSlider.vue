<template>
    <div class="my-5 d-flex justify-content-end align-items-center">
        <nav aria-label="Page navigation example">
            <ul class="pagination">
                <li class="page-item">
                    <a class="page-link dm-slide" href="#" aria-label="Previous">
                        <span class="dm-wt" aria-hidden="true"><i class="fa-solid fa-chevron-left"></i></span>
                    </a>
                </li>
                <li v-for="(num, index) in pages" :key="'pages'+index" class="page-item">
                    <a class="page-link dm-slide" href="#">{{num.number}}</a>
                </li>                
                <li class="page-item">
                    <a class="page-link dm-slide" href="#" aria-label="Next">
                        <span class="dm-wt" aria-hidden="true"><i class="fa-solid fa-chevron-right"></i></span>
                    </a>
                </li>
            </ul>
        </nav>
        
    </div>
</template>

<script>
export default {
    name: 'NumSlider',
    data(){
        return{
            pages: [
                {
                    number: 1,
                    activePage: false
                },
                {
                    number: 2,
                    activePage: false
                },
                {
                    number: 3,
                    activePage: false
                },
            ],
            
        }
    },
    
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-slide{
    &:hover{
        background-color: $bg-color-5!important;
        color: $font-color-1!important;
    }
}

</style>