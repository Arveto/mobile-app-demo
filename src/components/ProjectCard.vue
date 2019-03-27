<template>
  <div class="card-expansion">

    <md-card>
      <md-card-media>
        <img src="../assets/logo.png" alt="img">
      </md-card-media>

      <md-card-header>
        <div class="md-title"> {{ project.name }} </div>
        <div class="md-subhead"> {{ project.description }} </div>
      </md-card-header>

      <md-card-expand>
        <md-card-actions md-alignment="space-between">
          <div></div>
          <md-card-expand-trigger>
            <md-button>Plus</md-button>
          </md-card-expand-trigger>
          <div></div>
        </md-card-actions>

        <md-card-expand-content>
          <md-card-content>
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Optio itaque ea, nostrum odio. Dolores, sed accusantium quasi non, voluptas eius illo quas, saepe voluptate pariatur in deleniti minus sint. Excepturi.
          </md-card-content>
        </md-card-expand-content>
      </md-card-expand>
    </md-card>
  </div>
</template>

<script>
  export default {
    name: 'ProjectCard',
    props: ['project']
  }
</script>

<style lang="scss" scoped>
  img{
    max-height: 100px !important; //trapper's trick
    width: auto !important;
  }

  .card-expansion {
    // height: 480px;
  }

  .md-card {
    width: 320px;
    margin: 4px;
    display: inline-block;
    vertical-align: top;
  }
</style>
