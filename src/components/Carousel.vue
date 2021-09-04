<template>
    <b-carousel
        controls
        fade
        indicators
        img-width=""
        label-next=""
        label-prev=""
    >
        <div v-for='slide in slides'
        :key='slide.id'>
            <b-carousel-slide class='slide-style' :caption='slide.caption' :text="slide.text" :img-src='slide.img'> <b-button :to='slide.link' variant="outline-light">Read More</b-button></b-carousel-slide>
        </div>
    </b-carousel>
</template>

<script>
export default {
    name: 'Carousel',
    props: {

    },
    data() {
        return {
            slides: [
                    {
                        id: '1',
                        img: require('@/assets/group_pic_1.jpg'),
                        caption: 'What is MTOP?',
                        text: 'The Milwaukee Trauma Outcomes Project (MTOP) is a consortium dedicated to improving the lives of those affected by trauma through research, intervention, prevention, education, and outreach.',
                        link: '/about',
                    },
                    {
                        id: '2',
                        img: require('@/assets/trauma1.jpeg'),
                        caption: 'Why trauma?',
                        text: 'Approximately 90% of people in the United States are exposed to at least one traumatic event during their lifetime, most of whom are exposed to an average of 4 traumatic events.',
                        link: '/about',
                    },
                    {
                        id: '3',
                        img: require('@/assets/group_pic_2.jpg'),
                        caption: 'Who are we?',
                        text: '',
                        link: '/people',
                    }
                    ]
        }
    }


}
</script>

<style scoped>
.slide-style {
    background-color: black;
}
</style>