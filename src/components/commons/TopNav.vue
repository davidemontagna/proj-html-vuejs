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
.container{
    span{
        color: #b7b7b7;
    }
}

.dm-nav-top{
    width: 30%;
    margin-left: 20px;
    .dm-nav-links{
        text-transform: uppercase;
        color: #fff;
        text-decoration: none;

        &:hover{
            color: #b7b7b7;
        }        
    }
    
}
</style>