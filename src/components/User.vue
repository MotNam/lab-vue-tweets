<template>
<div>
 <span className="user">
  <span className="name">{{ user.name }} </span>
  <span className="handle">@{{ user.handle }}</span>
</span>
</div>
 
</template>

<script>
export default {
  name: 'User',
  props: {
    user: {
      name: {
        type: String
      },
      handle:{
        type: String
      },
      
    },
    },
  };
</script>

<style>

</style>