<template>
    <nav class="container">
        <div class="d-flex justify-content-start">
            <span>Everything about Lifestyle, Travel and Gadgets!</span>             
                
            <div class="dm-nav-top d-flex justify-content-evenly">
                <a 
                v-for="element in topNav"
                :key="element"
                class="dm-nav-links" 
                href="#">
                {{element}}
                </a>                        
            </div>
                
        </div>
    </nav>
</template>

<script>
export default {
    name: 'TopNav',
    data(){
        return{
            topNav: ['sign in', 'about us', 'contact us', 'buy now']
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.container{
    span{
        color: $font-color-2;
    }
}

.dm-nav-top{
    width: 30%;
    margin-left: 20px;
    .dm-nav-links{
        text-transform: uppercase;
        color: $font-color-1;
        text-decoration: none;

        &:hover{
            color: $font-color-2;
        }        
    }
    
}
</style>