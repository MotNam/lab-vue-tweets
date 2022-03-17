<template>
<div>
 <span className="user">
  <span className="name">{{ tweet.user.name }} </span>
  <span className="handle">@{{ tweet.user.handle }}</span>
</span>
</div>
 
</template>

<script>
export default {
  name: 'User',
  props: {
    user: Object
    },
  };
</script>

<style>

</style>