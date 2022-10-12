<template>
  <span className="user">
    <span className="name">{{ user.name }}</span>
    <span className="handle">{{ user.handle }}</span>
  </span>

      <!-- <Timestamp :timestamp="timestamp" /> -->

  </template>
  
  <script>
  import Timestamp from "./Timestamp.vue";

  export default {
    props: {
      user: Object,
      timestamp: String,
    },
    components: { Timestamp },
  };
  </script>
  
  <style></style>