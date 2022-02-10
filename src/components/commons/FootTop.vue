<template>
    <section class="d-flex justify-content-between my-5 pb-5">
        <div class="dm-about">
            <h6 class="text-uppercase fw-bold">About the blog</h6>
            <div class="my-3">
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsa consequatur illum placeat pariatur sequi optio modi. Alias commodi qui quibusdam!</p>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis doloremque accusantium, est aliquam cupiditate laborum atque, dolore natus velit numquam deleniti. Mollitia, pariatur.</p>
                
            </div>
            <h6 class="dm-view-more fw-bold text-uppercase"><a href="#">View More <i class="fa-solid fa-chevron-right"></i></a></h6>
        </div>

        <div class="dm-recent-pst mx-5">
            <h6 class="text-uppercase fw-bold">Recent posts</h6>
            <div class="d-flex justify-content-between my-3" v-for="(post, index) in footRecPosts" :key="index">
                <div class="dm-recent-img">
                    <img :src="require(`../../assets/img/recent-posts/${post.img}.jpg`)" alt="">
                </div>
                <div class="fw-bold ms-3 dm-recent-txt">
                    <p>{{post.text}}</p>
                    <span class="fw-light">{{post.date}}</span>
                </div>
            </div>
        </div>

        <div class="dm-recent-comments">
            <h6 class="text-uppercase fw-bold">Recent comments</h6>
            <div class="my-3" v-for="(comment, index) in recentComments" :key="'comm'+index">
                <p>
                    <span class="dm-arrow-rec-comments"><i class="fa-solid fa-chevron-right"></i></span>
                    {{comment.author}}
                    <span>commented on </span> 
                    <a class="fw-bold" href="#">{{comment.link}}</a>
                </p>
                <span class="dm-rec-comm-date">{{comment.date}}</span>
            </div>
        </div>

        <div class="dm-categories ms-5">
            <h6 class="text-uppercase fw-bold">Categories</h6>
            <ul class="d-flex justify-content-start flex-wrap my-3">
                <li class="dm-category-list me-2 mt-3" v-for="(category, index) in categories" :key="'cat'+index">
                    <a href="#">{{category}}</a>
                </li>
                
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'FootTop',
    data(){
        return{
            footRecPosts:[
                {
                    img: 'our-office-4-square',
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                    date: '12:53 AM Dec 19th'
                },
                {
                    img: 'our-office-5-square',
                    text: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                    date: '12:53 AM Dec 19th'
                }
            ],
            recentComments:[
                {
                    author: 'John Doe',
                    link: 'Lorem ipsum dolor sit amet.',
                    date: '12:55 AM Dec 19th'
                },
                {
                    author: 'John Doe',
                    link: 'Lorem ipsum dolor sit amet.',
                    date: '12:55 AM Dec 19th'
                }
            ],
            categories:['Gadgets', 'Photography', 'Lifestyle', 'Fashion', 'Recipes', 'Travel', 'Business', 'Architecture', 'Reviews', 'Sports', 'Videos', 'Technology', 'Design'],
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-about{
    width: 35%;
    div p{
        font-size: 13px;
        color: $font-color-5;
    }
}

.dm-recent-pst{
    width: 25%;
}

.dm-recent-comments{
    width: 25%;

    div{
        p{
            font-size: 13px;
            color: $font-color-1;
            a{
                text-decoration: none;
                color: $font-color-4;
            }
            
        }
    }
}

.dm-rec-comm-date{
    color: $font-color-5!important;
    font-size: 11px!important;
}

.dm-arrow-rec-comments{
    color: $font-color-4!important;
    font-size: 11px!important;
}

.dm-recent-img{

    img{
        border-radius: 50%;
        height: 90px;
    }
    
}

h6{
    color: $font-color-1;
}

.dm-recent-txt{

    p{
        margin-bottom: 0;
        color: $font-color-2;
        font-size: 13px;
    }
    span{
        color: $font-color-5;
        font-size: 11px;
    }
}

.dm-categories{
    width: 20%;

    ul{
        padding: 0;
    }
}

.dm-category-list{
    list-style: none;
    

    a{
        padding: 6px;
        text-decoration: none;
        background-color: $bg-color-13;
        border-radius: 5px;
        color: $font-color-1;
        font-size: 13px;
        font-weight: bold;

        &:hover{
            color: $font-color-4;
        }
    }
}

.dm-view-more{
    a{
        color: $font-color-1;
        text-decoration: none;

        &:hover{
            color: $font-color-4;
        }
    }
}
</style>