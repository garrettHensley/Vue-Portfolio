<template>
  <div>
    <b-container id="job-container">
      <b-row align-v="stretch">
        <b-col>
          <b-list-group>
            <b-list-group-item
              v-for="(app, index) in apps"
              :key="app.key"
              @click="selectApp(app, index)
              "
              class="clickable"
              :class="{ 'bg-second': show === index, 'bg-main': show != index }"
            >
              <div class="py-2 lead">{{ app.name }}</div>
            </b-list-group-item>
          </b-list-group>
        </b-col>
        <transition name="slide-fade">
          <b-col class="bg-second shadows-second rounded">
            <Job :app="selectedApp" class="bg-second" />
          </b-col>
        </transition>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Job from "@/components/Job.vue";
import { apps } from "@/assets/Apps/apps.json";

export default {
  components: {
    Job
  },
  data() {
    return {
      apps: apps,
      selectedApp: {},
      show: 0
    };
  },
  mounted() {
    this.selectedApp = this.apps[0];
  },
  methods: {
    selectApp(app, index) {
      this.selectedApp = app;
      this.show = index;
    }
  }
};
</script>

<style scoped>
#job-container {
  padding-left: 0 !important;
}

.bg-second {
  opacity: 0.9;
}
.clickable {
  cursor: pointer;
}
</style>
