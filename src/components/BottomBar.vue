
<template>
  <div id="bottombar">
      <md-bottom-bar class="md-accent" md-type="shift">
        <md-bottom-bar-item md-label="Home" md-icon="home" @click="$emit('changeTab', 0)"></md-bottom-bar-item>
        <md-bottom-bar-item md-label="Pages" md-icon="pages" @click="$emit('changeTab', 1)"></md-bottom-bar-item>
        <md-bottom-bar-item md-label="Chat" md-icon="chat" @click="$emit('changeTab', 2)"></md-bottom-bar-item>
        <md-bottom-bar-item md-label="Favorites" md-icon="favorite" @click="$emit('changeTab', 3)"></md-bottom-bar-item>
      </md-bottom-bar>
  </div>
</template>

<script>
  export default {
    name: 'BottomBar',
    data: () => ({
    }),
    props: ['newMessage'],
    methods: {
    },
    mounted () {
    }
  }
</script>

<style lang="scss" scoped>

  #bottombar{
    width: 100%;
  }

  .badge {
    width: 19px;
    height: 19px;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    top: 6px;
    right: 6px;
    background: #fff;
    border-radius: 100%;
    color: #000;
    font-size: 10px;
    font-style: normal;
    font-weight: 600;
    letter-spacing: -.05em;
    font-family: 'Roboto Mono', monospace;
  }
</style>
