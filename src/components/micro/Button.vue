<template>

    <div class="dm-border-btn d-flex justify-content-center">
        <a class="dm-single-btn text-uppercase" href="#">{{button}}</a>
    </div>       
    
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

.dm-border-btn{
    width: 160px;
    background-color: $bg-color-8;
    padding: 10px;

    &:hover{
        border: 4px solid $bg-color-6;
    }
}

.dm-single-btn{   
    text-decoration: none;
    color: $font-color-1;
    
    &:hover{
        color: $font-color-1;
    }     
}
</style>