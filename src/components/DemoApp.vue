<template>
  <div class="page-container md-layout-column">
    <md-toolbar class="md-accent">
      <md-button class="md-icon-button" @click="showNavigation = true">
        <md-icon>menu</md-icon>
      </md-button>
      <span class="md-title">Arveto Ink.</span>

    </md-toolbar>

    <md-drawer :md-active.sync="showNavigation">
      <md-toolbar class="md-transparent" md-elevation="0">
        <span class="md-title">Showcase</span>
      </md-toolbar>

      <md-list>
        <md-list-item>
          <md-icon>move_to_inbox</md-icon>
          <span class="md-list-item-text">Download</span>
        </md-list-item>

        <md-list-item>
          <md-icon>send</md-icon>
          <span class="md-list-item-text">Send</span>
        </md-list-item>

        <md-list-item>
          <md-icon>delete</md-icon>
          <span class="md-list-item-text">Delete</span>
        </md-list-item>
      </md-list>
    </md-drawer>

    <md-content style="padding: 0;">
      <slot></slot>
    </md-content>

    <BottomBar :newMessage="newMessages" @changeTab="changeTab"/>
  </div>
</template>

<script>
  import BottomBar from './BottomBar.vue'

  export default {
    name: 'DemoApp',
    components: {
      BottomBar
    },
    data: () => ({
      newMessages: 3,

      showNavigation: false,
      showSidepanel: false
    }),
    methods: {
      changeTab(tab){
        this.$emit("changeTab", tab)
      }
    }
  }
</script>

<style lang="scss" scoped>
  .page-container {
    min-height: 667px;
    overflow: hidden;
    position: relative;
    border: 1px solid rgba(#000, .12);
  }

   // Demo purposes only
  .md-drawer {
    width: 230px;
    max-width: calc(100vw - 125px);
  }

  .md-content {
    padding: 16px;
    height: 560px;
  }
</style>
