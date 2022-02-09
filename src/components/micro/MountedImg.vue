<template>
    <img :src="require(`../../assets/img/big-posts-img/${img}.jpg`)" alt="">
</template>

<script>
export default {
    name: 'MountedImg',
    props:{
        img: String
    }
}
</script>

<style>

</style>