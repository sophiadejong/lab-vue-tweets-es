<template>
  <div className="tweet">
    <ProfileImage :image="tweet.user.image" />
    <div className="body">
      <div className="top">
        <User :user="tweet.user" :timestamp="tweet.timestamp" />
        <Timestamp :timestamp="tweet.timestamp" />
      </div>
      <Message :message="tweet.message" />
      <Actions :like="tweet.like" @like="$emit('like')" />
    </div>
    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import Message from "./Message.vue";
import Actions from "./Actions.vue";
import Timestamp from "./Timestamp.vue";

export default {
  props: {
    tweet: Object,
  },
  components: { ProfileImage, User, Message, Actions, Timestamp },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
