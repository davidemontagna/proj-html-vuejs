<template>
    <div class="d-flex justify-content-between flex-wrap">
        <div class="g-3 my-3 dm-lbl-container" v-for="(element, index) in labels" :key="index">
            <div class="dm-gradient"></div>
            <img :src="require(`../../assets/img/labels-img/${element.img}.jpg`)" alt="">
            
            <div class="dm-txt-labels p-2">
                <span class="dm-label">{{element.label}}</span>
                <span class="d-block my-2 dm-title">{{element.title}}</span>
                <p class="dm-text">{{element.text}}</p>
            </div>
        </div>        
    </div>
</template>

<script>
export default {
    name: 'LabelsGrid',
    data(){
        return{
            labels:[
                {
                    label: "Photography",
                    title: "How To Take Better Concert Pictures in 30 Seconds",
                    img: 'blog-46',
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis corrupti officiis veniam vitae at officia sed cumque reprehenderit animi iusto!"
                },
                {
                    label: "Gadgets",
                    title: "Gadgets That Make Your Smartphone Even Smarter",
                    img: 'blog-47',
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Minus provident consequatur a ipsa?"
                },
                {
                    label: "Travel",
                    title: "20 Top-Rated Tourist Attractions in Manhattan",
                    img: 'blog-48',
                    text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Commodi maxime illum magni officia! Incidunt, quos. Et optio aperiam quam maxime tenetur cumque magni perspiciatis!"
                },
                {
                    label: "Lifestyle",
                    title: "The Best Way to Ride a Motorcycle",
                    img: 'blog-49',
                    text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis corrupti officiis veniam vitae at officia sed cumque reprehenderit animi iusto!"
                },
                {
                    label: "Travel",
                    title: "5 Fun Things to Do at the Beach",
                    img: 'blog-50',
                    text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptate fugit, nemo aliquam quam quidem ad impedit voluptatem, asperiores nisi, fuga officia at deleniti! Magni illo, non deleniti voluptas alias dicta."
                },
                {
                    label: "Recipes",
                    title: "Amazingly Fresh Fruit And Herb Drinks For Summer",
                    img: 'blog-51',
                    text: "Lorem ipsum dolor sit, amet consectetur adipisicing elit. Odit, omnis repellat! Accusantium quod nisi omnis veniam."
                },
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-lbl-container{
    
    position: relative;

    img{
        height: 230px;
    }

    .dm-gradient{
        width: 100%;
        height: 100%;
        background-color: $bg-color-13;
        opacity: .2;
        position: absolute;
        top: 0;
        left: 0;
    }

    .dm-txt-labels{
        position: absolute;
        bottom: 10px;
        left: 10px;

        .dm-label{
            font-size: 12px;
            color: $font-color-1;
            text-transform: uppercase;
            padding: 10px;
            background-color: $bg-color-5;
        }

        .dm-title{
            color: $font-color-1;
            font-size: 20px;
            font-weight: bolder;
        }

        .dm-text{
            display: none;
            color: $font-color-2;
            font-size: 14px;
            font-weight: bold;
        }
    }

    &:hover .dm-text{
        display: block;        
    }
    &:hover .dm-gradient{
        opacity: .6;
        transition: .6s;
    }
}



</style>