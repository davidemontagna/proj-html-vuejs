<template>  
    <div class="container">
        <div class="row">
            <div class="col">
                <div class="dm-nav-bottom d-flex justify-content-between align-items-center">
                    <ul class="d-flex justify-content-start">
                        <li v-for="element in bottomNav" :key="element">
                            <a                         
                            class="dm-nav-links-btm" 
                            href="#">
                            {{element}}
                            </a> 

                        </li>
                    </ul>
                    

                    <search-bar />                       
                </div>

            </div>
        </div>
    </div>
</template>

<script>
import SearchBar from "./SearchBar.vue"

export default {
    name: 'BottomNav',
    components: {
        SearchBar,
    },
    data(){
        return{
            bottomNav: ['home', 'elements', 'features', 'pages', 'portfolio', 'blog', 'shop']
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-nav-bottom{

    ul{
        padding: 0;
        margin: 0;
        li{
            list-style: none;
        }
    }

    .dm-nav-links-btm{
        font-size: 17px;
        font-weight: bold;
        margin-right: 40px;
        text-transform: uppercase;
        color: $font-color-9;
        text-decoration: none;

        &:hover{
            color: $font-color-4;
        }        
    }
}
</style>