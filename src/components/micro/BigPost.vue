<template>
    <div class="dm-single-post my-4">
        <div class="dm-images">
            <mounted-img
            v-for="(img, e) in post.image"
            :key="e"
            :img="img"
            />
        </div>
        
        <div class="dm-post-data mt-3 d-flex justify-content-start">
            <div class="dm-date text-center">
                <div class="dm-day">{{post.dayDate}}</div>
                <div class="dm-month text-uppercase">{{post.month}}</div>
            </div>
            <div class="dm-post-desc ms-3 dm-wrapper">
                <h3>{{post.title}}</h3>
                <p class="dm-demo-1">{{post.text}}</p>
                <div class="dm-post-labels d-flex justify-content-start">
                    <span>
                        <i class="fa-regular fa-user"></i>
                        By <a href="#">{{post.author}}</a>
                    </span>
                    <span class="mx-3">
                        <i class="fa-regular fa-folder"></i>
                        <a v-for="(lbl, i) in post.label" :key="i" href="#"> {{lbl}} </a>
                    </span>
                    <span >
                        <i class="fa-regular fa-comments"></i>
                        <a href="#"> {{post.comments}} Comments</a>
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import MountedImg from "./MountedImg.vue"

export default {
    name: 'BigPost',
    components:{
        MountedImg
    },
    props: {
        post: Object
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-single-post{
    width: 100%;   

    img{
        height: 344px;
    }

    &:hover .dm-demo-1{
        display: block;

    }
}

.dm-post-desc{
    border-bottom: 1px solid $border-color-3;
    padding-bottom: 24px;    
}

.dm-wrapper{
    
    overflow: hidden;
    text-overflow: ellipsis;



    .dm-demo-1 {
        overflow: hidden;
        display: -webkit-box;
        -webkit-line-clamp: 3;
        -webkit-box-orient: vertical;
    }
}

.dm-day{
    height: 40px;
    line-height: 40px;
    background-color: $bg-color-3;
    padding: 3px;
}

.dm-month{
    font-size: 12px;
    color: $font-color-1;
    background-color: $bg-color-13;
    padding: 3px 10px;
}

.dm-post-labels{
    width: 100%;
    font-size: 13px;

    span {
        color: $font-color-5;

        a{
        text-decoration: none;
        }
    }
}

.dm-single-post:last-child{
    img{
        height: 275px;
    }
}
</style>