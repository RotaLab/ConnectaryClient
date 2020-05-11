<template>
  <div class="home">
    <Toolbar />
    <div class="home__wrapper">

    </div>
  </div>
</template>

<script>
import Toolbar from '@/components/Toolbar/Toolbar.vue'

export default {
  name: 'Home',
  components: {
    Toolbar,
  },
  methods: {
    selectProject(project) {
      this.selectedProject = project;
    },
    deselectProject() {
      this.selectedProject = {};
    }
  },
  data() {
    return {
      selectedProject: {}
    }
  }
}
</script>

<style scoped lang="scss">
  .home {
    
    &__wrapper {
      display: flex;
      max-width: 1080px;
      width: 90%;
      margin: spacing(4) auto;
      height: calc(100vh - 70px - #{spacing(4)} * 2);
    }

    &__projects,
    &__project-view {
      height: 100%;
    }

    &__project-view {
      margin-left: spacing(4);
      flex-grow: 1;
    }
  }
</style>