<template>
  <section class="dm-small-posts d-flex justify-content-between">
      
        <div class="mt-4 fw-bold" >
          POPULAR POSTS
            <div class="dm-populars d-flex align-items-start justify-content-start" v-for="(element, index) in popularPosts" :key="'rec-'+index">
              
              <img :src="require(`../../assets/img/small-img-posts/${element.img}.jpg`)" alt="">
                <div class="ms-2">
                    <span class="mb-3 dm-txt-post">{{element.text}}</span>
                    <span class="d-block dm-date">{{element.date}}</span>
                </div>
            </div>         
          
        </div>
        <div class="ms-3 mt-4 fw-bold" >
            POPULAR POSTS
            <div class="dm-populars d-flex align-items-start justify-content-start" v-for="(element, index) in recentPosts" :key="'pop-'+index">               
                <img :src="require(`../../assets/img/small-img-posts/${element.img}.jpg`)" alt="">
                    <div class="ms-2">
                        <span class="mb-3 dm-txt-post">{{element.text}}</span>
                        <span class="d-block dm-date">{{element.date}}</span>
                    </div>
            </div>         
            
        </div>
        <div class="mt-4 d-flex flex-column justify-content-between">
            <div class="fw-bold">
                FEATURED POSTS
                <div class="mt-5 dm-featured d-flex align-items-start justify-content-start">  
                    <div class="dm-gradient"></div>             
                    <img src="../../assets/img/small-img-posts/blog-66.jpg" alt="">
                    <div class="dm-txt-labels">
                    
                        <span class="dm-label text-uppercase">recipes</span>
                        <span class="d-block my-2 dm-title">Tips to Help You Quickly Prepare your Lunch</span>
                        <p class="dm-text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ducimus, delectus.</p>
                    </div>
                </div> 
            </div>

            <div class="fw-bold mt-5">
                FEATURED AUTHOR
                <div class="dm-author mt-5 d-flex justify-content-between" v-for="(avatar, index) in authors" :key="'avatar'+index">
                    <img :src="require(`../../assets/img/avatars-img/${avatar.image}.jpg`)" alt="">
                    <div class="ms-4 dm-avatar-data">
                        <span class="d-block dm-name-avatar">{{avatar.author}}</span>
                        <span class="mt-2 fw-light d-block dm-avatar-desc">{{avatar.description}}</span>
                    </div>
                </div>
            </div>
                 
        </div>
  </section>
</template>

<script>
export default {
    name: 'AllPosts',
    data(){
        return{
            popularPosts: [
                {
                    text: 'Simple Ways to Have a Pretty Face',
                    img: 'blog-55',
                    date: 'January 12, 2019'
                },
                {
                    text: 'Ranking the greatest players in basketball',
                    img: 'blog-56',
                    date: 'January 12, 2019'
                },
                {
                    text: '4 Ways to Look Cool in Glasses',
                    img: 'blog-57',
                    date: 'January 12, 2019'
                },
                {
                    text: 'Top Camper Trailer Towing Tips',
                    img: 'blog-58',
                    date: 'January 12, 2019'
                },
                {
                    text: '5 Lovely Walks in New York',
                    img: 'blog-59',
                    date: 'January 12, 2019'
                }
            ],
            recentPosts: [
                {
                    text: 'Main Reasons To Stop Texting And Driving',
                    img: 'blog-65',
                    date: 'January 12, 2019'
                },
                {
                    text: 'Tips to Help You Quickly Prepare your Lunch',
                    img: 'blog-66',
                    date: 'January 12, 2019'
                },
                {
                    text: 'Why should I buy a smartwatch?',
                    img: 'blog-67',
                    date: 'January 12, 2019'
                },
                {
                    text: 'The best augmented reality smartglasses',
                    img: 'blog-68',
                    date: 'January 12, 2019'
                },
                {
                    text: '12 Healthiest Foods to Eat for Breackfast',
                    img: 'blog-69',
                    date: 'January 12, 2019'
                },
            ],
            authors: [
                {
                    author: 'John Doe',
                    image: 'avatar',
                    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Maiores minima nihil hic ut laudantium?'
                }
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-small-posts{
    width: 100%;
}

.dm-populars{
    padding: 20px 0;
    font-size: 11px;
    border-bottom: 1px solid $border-color-4;

    &:last-child{
        border-bottom: none;
    }

    .dm-txt-post{
        color: $font-color-8;
        font-size: 13px;
    }

    img{
        height: 70px;
        width: 70px;
        object-fit: cover;
    }
}

.dm-featured{
    position: relative;

    .dm-gradient{
        width: 100%;
        height: 100%;
        background-color: $bg-color-13;
        opacity: .2;
        position: absolute;
        top: 0;
        left: 0;
    }

    img{
        height: 170px;
    }

    .dm-txt-labels{
        position: absolute;
        bottom: 5px;
        left: 20px;

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
            font-size: 11px;
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

.dm-author{

    img{
        height: 150px;
    }

    .dm-avatar-data{
        width: 230px;
        
        .dm-name-avatar{
            font-size: 18px;
            color: $font-color-10;
        }

        .dm-avatar-desc{
            font-size: 14px;
            color: $font-color-3;
        }
    }
}
</style>