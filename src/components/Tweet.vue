<template>
  <div className="tweet">
  
    <ProfileImage :image="tweet.user.image" />

    <div className="body">
      <div className="top">
    
      <User :user="tweet.user"/>

        <Timestamp :timestamp="tweet.timestamp" />

      </div>

     
       <Message :message="tweet.message" />

      <Actions />

    </div>

    <i class="fas fa-ellipsis-h"></i> 
    <!-- <button @click="log">Console log</button> -->
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue'
import User from './User.vue'
import Timestamp from './Timestamp.vue'
import Message from './Message.vue'
import Actions from './Actions.vue'

export default {
name: 'Tweet',
methods: {
  log() {
    console.log(this.tweet)
  }
},
   props: {
     tweet: {
         type: Object,
       }
    },
   
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions,
  },
};


</script>

<style scoped>
a {
  color: #42b983;
}
</style>
