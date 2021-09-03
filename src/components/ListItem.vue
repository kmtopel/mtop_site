<template>
    <li class='listItemBody'>
        <b-container>
            <b-row>
                <h6>{{title}}</h6>
            </b-row>
            <b-row>
                <p>{{text}}</p>
            </b-row>
        </b-container>
    </li>
</template>

<script>
export default {
    name: 'ListItem',
    props: {
        title: String,
        text: String,
    }
}
</script>

<style scoped>
.listItemBody {
    
    margin-top: 10px;
}
li {
    text-decoration: none;
    text-align: left;
}
h6 {
    text-align: center;
}
</style>