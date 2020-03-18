<template>
        <div class ="container" :class="[this.ToogleView? 'card':'list']"> 
            <Tweet v-for="(tweet,list) in tweets" :key="list" :tweetFeed="tweet"/>
    </div>
</template>

<script>
import Tweet from './Tweet.vue'
    export default {
        name: "TweetCards",
        components: {
            Tweet,

        },
        mounted() {
            this.$root.$on("switch", this.SwitchView);
        },
        methods: {
            SwitchView(){
            if(this.ToogleView){
                this.ToogleView = false;
            } else {
                this.ToogleView = true;
            }

        },
    },

    data(){
        return {
            tweets: [

                  {
        author: 'Zeefah Inamus',
        content:' Interesting times we live in..'

      },

      {
        author: 'George Bush',
        content:' Fool me once..shame on.. how does it go again '

      },

      {
        author: 'Danny Glover',
        content:' Getting way too old for this ish'

      },

      {
        author: 'Alex ',
        content: 'Gandhi says... COOOOODDDEEEEE '

      },

      {
        author: 'Weezy',
        content: 'We are not the same.. I am a Martian'

      },

      {
        author: 'Feez',
        content: "I'm coding.. yet I don't feel like I know what I am doing... its a mind fuk"

      },

         ],
         ToogleView: true,
        };
    },

} 
</script>

<style scoped>
.container{
    display: grid;
        gap: 5px;
        width: 80vw;
        height: 70vh;
        border: 2px solid black;
}

 .card{
        grid-template-columns:repeat( auto-fill, minmax(200px, 1fr) );
       
    }
    .list{
        grid-template-columns: 1fr;
    }

</style>