<template>
    <b-nav-item :to='url'><span class='navBtn'>{{text}}</span></b-nav-item> 
</template>

<script>
export default {
    name: 'NavBtn',
    props: {
        url: String,
        text: String,
    }
}
</script>

<style scoped>
.navBtn {
    text-decoration: none;
    color: black;
    font-size: 125%;
    font-weight: ;
}
</style>