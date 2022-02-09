<template>
    <div class="dm-buttons d-flex justify-content-evenly align-items-center">
        <i class="fa-solid fa-chevron-left"></i>
        <Button 
        v-for="(button, index) in buttons"
        :key="index"
        :button="button"
        />
        <i class="fa-solid fa-chevron-right"></i>
    </div>
</template>

<script>
import Button from "../micro/Button.vue"

export default {
    name: 'Buttons',
    components: {
        Button
    },
    data(){
        return{
            buttons:['Gadgets', 'Photography', 'Lifestyle', 'Fashion', 'Recipes', 'Travel']
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-buttons{
    height: 100px;
    width: 100%;    
}
</style>