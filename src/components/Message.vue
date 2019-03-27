<template>
  <div class="message">

    <div class="metamessage">
      <md-avatar>
        <img src="../assets/alberto.jpg" alt="Avatar">
      </md-avatar>
    </div>

    <div class="content" :class="message.sender">
      <p>{{message.content}}</p>
    </div>

    <p class="sender">{{message.from}}</p>
  </div>
</template>

<script>
export default {
  name: "Message",
  props: [ 'message' ]
}
</script>

<style lang="css" scoped>
  .message{
    display: flex;
    padding-top: 20px;
  }
  .sender{
    position: absolute;
    left: 50px;
    margin-top: -20px;
    color: grey;
  }
  .metamessage{
    display: block;
    flex: flex-end;
    margin-top: -10px;
  }
  .content{
    display: block;
    clear: both;
    padding: 0 15px 0 15px;
    border-radius: 30px;
  }
  .notme{
    background-color: rgb(45, 45, 45);
    float: left;
  }
  .me{
    float: right;
    background: #0084ff;
    color: #fff;
  }
</style>
