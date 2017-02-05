<template>
  <div class="top">
    <p>
      Signed in as  <a href=""><b>{{username}}</b></a>
      <a href="" class="signout"> Sign out</a>
    </p>
  </div>
</template>

<script>
export default {
  data () {
    return {
      username: 'Admin'
    }
  }
}
</script>

<style lang="stylus">
  .top {
    display: flex;
    justify-content: flex-end;
    padding: 20px;
    
    .signout {
      margin-left: 20px;
    }
  }
</style>
