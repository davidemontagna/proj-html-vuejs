<template>
    <section>
        <div class="dm-socials my-4">
            <div class="dm-twitter">
                <span class="text-uppercase fw-bold">Latest from twitter</span>
                <div class="dm-tweet mt-2 mb-3 d-flex justify-content-between" v-for="(tweet, index) in twitterPosts" :key="index">
                    <div class="dm-twitter-icon">
                        <i class="fa-brands fa-twitter"></i>
                    </div>
                    <div class="dm-tweet-txt ms-2">
                        <p>{{tweet.text}}</p>
                        <span>{{tweet.date}}</span>
                    </div>
                </div>
            </div>
            <div class="dm-instagram my-4">
                <span class="text-uppercase fw-bold">Photos from instagram</span>
                <div class="my-3">
                    <img :src="require(`../../assets/img/img-instagram/${photo}.jpg`)"
                    alt=""
                    v-for="(photo, index) in photoInstagram"
                    :key="'photo'+index"
                    >
                </div>
            </div>
            <div class="dm-tags mb-5">
                <span class="text-uppercase fw-bold">Tags</span>
                <div class="dm-tag my-3 text-uppercase fw-bold  d-flex justify-content-between">
                    <a v-for="tag in tags"
                    :key="'tag'+tag"
                    href="#">
                    {{tag}}
                    </a>
                </div>
            </div>
            <div class="dm-facebook">
                <span class="text-uppercase fw-bold">Find us on Facebook</span>
                <div class="dm-fb-link">
                    <a href="#">Okler Themes</a>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Socials',
    data(){
        return{
            twitterPosts: [
                {
                    text: 'If you have any suggestions for the next updates, let us know.',
                    date: '01:05 PM Sep 18th',
                },
                {
                    text: 'We have just updated Porto Admin. Check the changelog for more information',
                    date: '01:04 PM Sep 18th',
                },
            ],
            photoInstagram: ['29739607_2020680068220520_4509928046932787200_n', '30087804_253872848488989_8792603541668626432_n', '29415620_196477127626244_3250318472361541632_n', '30078414_1274410412703843_8290935809419247616_n', '30077195_2066750973610181_3733150062893596672_n', '29415304_166583630713703_1032667922171953152_n',],
            tags: ['design', 'brands', 'video', 'business', 'travel']
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';

.dm-twitter, .dm-instagram, .dm-tags, .dm-facebook{
    
    span{
        font-size: 14px;
        color: $font-color-10;
    }
}

.dm-facebook{
    margin-top: 80px;

    .dm-fb-link{
        padding: 10px;
        border-left: 3px solid $border-color-5;

        a{
            padding-left: 5px;
            text-decoration: none;
            font-weight: bold;
            color: $font-color-4;
        }
    }
}

.dm-twitter-icon{
     font-size: 15px;
}

.dm-tweet-txt{
    p{
       color: $font-color-3;
       font-size: 17px;
       margin-bottom: 0;
    }

    span{
        color: $font-color-4;
        font-size: 12px;
    }
}

.dm-instagram{
    img{
        height: 115px;
    }
}

.dm-tag{
    

    a{
        font-size: 13px;
        color: $font-color-1;
        padding: 3px 8px;
        background-color: $bg-color-8;
        border-radius: 15px;
        text-decoration: none;


    }
}

</style>