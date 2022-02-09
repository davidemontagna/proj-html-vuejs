<template>
    <div class="dm-big-posts">
        <div>
            <big-post
            v-for="(post, index) in bigPost"
            :key="index"
            :post="post"
            />
        </div>
        <div>
            <num-slider />
        </div>
        
    </div>
</template>

<script>
import BigPost from "../micro/BigPost.vue";
import NumSlider from "../micro/NumSlider.vue"

export default {
    name: 'PostsBig',
    components: {
        BigPost,
        NumSlider
    },
    data(){
        return{
            bigPost: [
                {
                    title: 'How to Make Friends as a Grown-Up',
                    dayDate: '12',
                    month: 'Jan',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
                    image: ['blog-54'],
                    author: 'John Doe',
                    label: ['Lifestyle,', 'Travel'],
                    comments: 12
                },
                {
                    title: 'Simple Ways to Have a Pretty Face',
                    dayDate: '12',
                    month: 'Jan',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
                    image: ['blog-55 (1)'],
                    author: 'John Doe',
                    label: ['Photography,', 'Travel'],
                    comments: 12
                },
                {
                    title: 'Ranking the greatest players in basketball',
                    dayDate: '12',
                    month: 'Jan',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
                    image: ['blog-56 (1)'],
                    author: 'John Doe',
                    label: ['Sports,', 'Business'],
                    comments: 12
                },
                {
                    title: 'Top Camper Trailer Towing Tips',
                    dayDate: '12',
                    month: 'Jan',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
                    image: ['blog-58 (1)'],
                    author: 'John Doe',
                    label: ['Travel,', 'Lifestyle'],
                    comments: 12
                },
                {
                    title: '10 Best Travel Tips After 5 Years Traveling The World',
                    dayDate: '8',
                    month: 'Jan',
                    text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo. Nemo enim ipsam voluptatem quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
                    image: ['blog-13', 'blog-16', 'blog-20', 'blog-23', 'blog-29', 'blog-40'],
                    author: 'John Doe',
                    label: ['Travel,', 'Lifestyle'],
                    comments: 12
                },

            ]
        }
    }
}
</script>

<style lang="scss">
@import '../../assets/style/global.scss';


</style>