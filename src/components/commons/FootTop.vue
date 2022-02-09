<template>
    <section class="d-flex justify-content-between my-5">
        <div class="dm-about">
            <h6 class="text-uppercase fw-bold">About the blog</h6>
            <div class="my-3">
                <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Ipsa consequatur illum placeat pariatur sequi optio modi. Alias commodi qui quibusdam!</p>
                <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Perferendis doloremque accusantium, est aliquam cupiditate laborum atque, dolore natus velit numquam deleniti. Mollitia, pariatur.</p>
                
            </div>
            <h6 class="text-uppercase"><a href="#">View More <i class="fa-solid fa-chevron-right"></i></a></h6>
        </div>

        <div class="dm-recent-pst mx-5">
            <h6 class="text-uppercase fw-bold">Recent posts</h6>
            <div class="d-flex justify-content-between my-3" v-for="(post, index) in footRecPosts" :key="index">
                <div class="dm-recent-img">
                    <img :src="require(`../../assets/img/recent-posts/${post.img}.jpg`)" alt="">
                </div>
                <div class="fw-bold ms-3 dm-recent-txt">
                    <p>{{post.text}}</p>
                    <span>{{post.date}}</span>
                </div>
            </div>
        </div>

        <div class="dm-recent-comments">
            <h6 class="text-uppercase fw-bold">Recent comments</h6>
            <div class="my-3" v-for="(comment, index) in recentComments" :key="'comm'+index">
                <p><i class="fa-solid fa-chevron-right"></i> {{comment.author}} commented on <a href="#">{{comment.link}}</a> </p>
                <span>{{comment.date}}</span>
            </div>
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
            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-about{
    width: 35%;
    div p{
        color: $font-color-5;
    }
}

.dm-recent-pst{
    width: 25%;
}

.dm-recent-comments{
    widows: 25%;
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
        font-size: 15px;
    }
    span{
        color: $font-color-5;
        font-size: 13px;
    }
}
</style>