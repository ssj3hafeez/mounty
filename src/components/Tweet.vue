<template>
    <div id= "tweets">
        <h2>{{this.tweetFeed.author}}</h2>
        <H3>{{ this.tweetFeed.content }}</h3>
    </div>
</template>

<script>
    export default {
        name: "Tweet",
        props:  {
            tweetFeed: Object,
        }
    }
</script>

<style scoped>

#tweets{
        display: inline-block;
        border: 1px solid grey;
        padding: 5px;
        box-shadow: 3px 3px lightcoral;
    }

</style>