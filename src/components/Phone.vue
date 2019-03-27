<template>
  <div>
    <div class="phone-viewport">
      <DemoApp @changeTab="changeTab">

        <md-content v-if="currentTab==0" class="content">
          <!-- HOME -->
          <div style="text-align: center; padding: 8px;">
            <p class="md-title">Arveto Ink., la Junior Entreprise de l'ISTY</p>
            <img src="../assets/small.jpg" alt="">
            <br><br><br>
            <md-divider></md-divider>

            <p class="md-title">Donnez nous la chance de vous aider</p>
            <p style="text-align: left;">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
          </div>
        </md-content>

        <md-content v-if="currentTab==1" class="content">
          <!-- PROJECTS -->
          <p class="md-display-2" style="text-align: left; padding-left: 5px; margin-top: 5px;">
            Powered by :
          </p>
          <ProjectCard v-for="project in projects" :key="project.id" :project="project"/>
        </md-content>

        <md-content v-if="currentTab==2" class="content">
          <!-- CHAT -->
          <Messenger/>
        </md-content>

        <md-content v-if="currentTab==3" class="content">
          <!-- LOVE -->
          <md-card class="md-card-example" style="margin: 10px;">
            <br>
            <md-card-area md-inset>
              <md-card-media>
                <img src="../assets/small.jpg" alt="Arveto Ink.">
              </md-card-media>

              <md-card-header>
                <h2 class="md-title">Arveto Ink.</h2>
                <div class="md-subhead">
                  <span>ISTY Junior Entremprise</span><br>
                </div>
              </md-card-header>

              <md-card-content>
                A bientôt :)
              </md-card-content>
            </md-card-area>

            <md-card-content>
              <h3 class="md-subheading">Suivez nous !</h3>
              <div class="card-reservation">
                <div class="md-button-group">
                  <md-button :href="'https://github.com/Arveto'">github</md-button>
                  <md-button :href="'https://twitter.com/ArvetoSoftwares'">twitter</md-button>
                </div>
              </div>
            </md-card-content>

            <md-card-actions>
              <md-button class="md-primary">Nous contacter</md-button>
            </md-card-actions>
          </md-card>
        </md-content>
      </DemoApp>
    </div>
  </div>
</template>

<script>
  import DemoApp from './DemoApp.vue'
  import ProjectCard from './ProjectCard.vue'
  import Messenger from './Messenger.vue'

  export default {
    name: 'Phone',
    components: {
      DemoApp, ProjectCard, Messenger
    },
    data: () => ({
      checkInterval: null,
      currentTab: 0,

      projects: [
        {
          id: 0,
          name: "Vue.js",
          description: "",
          github: "vuejs.com"
        },
        {
          id: 1,
          name: "Material Design",
          description: "",
          github: "http://github.com/Arveto/bite"
        }

      ]
    }),
    methods: {
      changeTab(tab){
        this.$data.currentTab = tab;
      }
    },
    mounted () {
    }
  }
</script>

<style lang="css" scoped>
  .phone-viewport {
    width: 375px;
    height: 667px;
    overflow: hidden;
    border: 1px solid rgba(#000, .26);
    box-shadow: 0 0 20px 10px rgba(0,0,0,.2);
    border-radius: 20px;
    background: rgba(#000, .06);

    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  .content{
    overflow-y: auto;
    height: 100%;
    text-align: center;
    padding-top: 10px;
  }

  img{
    border-radius: 5px;
    max-width: 50%;
  }
</style>
