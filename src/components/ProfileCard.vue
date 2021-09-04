<template>
  <b-link :to='url' append>
    <b-card 
        text-variant="dark"
        :url='url'
        :title='name'
        :sub-title='role'
        border-variant='light'
        class='px-0 mx-0'
        >
        <b-card-body class='p-0 m-0'>            
            <b-row>
                <b-img thumbnail rounded  :src='image'></b-img>    
            </b-row>
        </b-card-body> 
    </b-card>
  </b-link>
</template>

<script>
export default {
    name:'ProfileCard',
    props: {
        name: String,
        role: String,
        bio: String,
        image: String,
        url: String,
        data: Object,
    }
}
</script>

<style>
a {
    text-decoration: none;
}

</style>