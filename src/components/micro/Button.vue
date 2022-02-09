<template>

    <a class="dm-single-btn text-uppercase" href="#">{{button}}</a>          
    
</template>

<script>
export default {
    name: 'Button',
    props: {
        button: String
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';


.dm-single-btn{   
    text-decoration: none;
    color: $font-color-1;
    width: 160px;
    background-color: $bg-color-8;
    padding: 10px;
    text-align: center;
    
    
    &:hover{
        border: 4px solid $bg-color-6;
        color: $font-color-1;
    }     
}
</style>