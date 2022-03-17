<template>
  <div className="tweet">
    <!-- <img
      :src="tweet.user.image"
      className="profile"
      alt="profile"
    /> -->
    <ProfileImage :image="user.image" />

    <div className="body">
      <div className="top">
      <!-- <span className="user">
          <span className="name">{{ tweet.user.name }}</span>
          <span className="handle">@{{ tweet.user.handle }}</span>
      </span> -->
      <User :user="user"/>

        <!-- <span className="timestamp">{{ tweet.timestamp }}</span> -->
        <Timestamp :time="timestamp" />

      </div>

      <!-- <p className="message">{{ tweet.message }}
      </p> -->
       <Message :message="message" />

      <!-- <div className="actions">
         Font Awesome icons -->
        <!-- <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>  -->

      <Actions />

    </div>

    <i class="fas fa-ellipsis-h"></i>
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

   props: {
     tweet: Object,
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
