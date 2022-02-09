<template>
    <div class="dm-slide my-5 d-flex justify-content-end align-items-center">
        <div>
            <i class="fa-solid fa-chevron-left" @click="goUp()"></i>
        </div>
        
        <div>
            <a 
            class="dm-slide-num mx-2"
            href="#"
            v-for="(num, index) in pages"
            :key="'pages'+index"
            >{{num.number}}</a>
        </div>
        <div>
            <i class="fa-solid fa-chevron-right"></i>
        </div>
        
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
            position: -1,
        }
    },
    methods:{
        goUp(){
            
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-slide{
    color: $font-color-4;
}

.dm-active{
    background-color: #0088cc;
    color: #fff;

    &:hover{
        color: #fff;
    }
}

.dm-slide-num{
    padding: 5px 8px;
    text-decoration: none;
    color: $font-color-4;
    text-align: center;

    &:hover{
        text-decoration: underline;
        color: $font-color-4;
    }
}
</style>