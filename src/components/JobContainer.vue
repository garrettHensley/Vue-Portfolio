<template>
  <div>
    <b-container id="job-container">
      <b-row align-v="stretch">
        <b-col>
          <b-list-group>
            <b-list-group-item
              v-for="(app, index) in apps"
              :key="app.key"
              @click="
                getSelection(
                  app.name,
                  app.description,
                  app.img,
                  app.source,
                  app.pages
                ),
                  (show = index)
              "
              class="clickable"
              :class="{ 'bg-second': show === index, 'bg-main': show != index }"
            >
              <p class="lead">
                {{ app.name }}
              </p>
            </b-list-group-item>
          </b-list-group>
        </b-col>
        <transition name="slide-fade">
          <b-col class="bg-second shadows-second rounded">
            <a :href="selectPages" target="_blank">
              <Job
                :name="selectName"
                :description="selectDescription"
                :image="selectImage"
                :link="selectLink"
                :pages="selectPages"
                class="bg-second"
              />
            </a>
          </b-col>
        </transition>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Job from "@/components/Job.vue";
import Apps from "@/assets/Apps/apps.json";


export default {
  components: {
    Job,
  },
  data() {
    return {
      apps: Apps.apps,
      selectName: null,
      selectDescription: null,
      selectImage: null,
      selectLink: null,
      selectPages: null,
      show: 0,
    };
  },
  mounted() {
    this.init();
  },
  methods: {
    init() {
      // Set default selection
      this.getSelection(
        this.apps[0].name,
        this.apps[0].description,
        this.apps[0].img,
        this.apps[0].source,
        this.apps[0].pages
      );
    },
    getSelection(name, description, image, link, pages) {
      // get data from selected job and send it to Job component
      this.selectName = name;
      this.selectDescription = description;
      this.selectImage = image;
      this.selectLink = link;
      this.selectPages = pages;
    },
  },
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
