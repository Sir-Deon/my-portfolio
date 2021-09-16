<template>
  <div>
    <v-card class="mx-auto my-5" width="400">
      <div class="carol">
        <img height="200" :src="project.pics[0]" />
      </div>

      <v-card-title>{{ project.title }}</v-card-title>

      <v-card-text>
        <div>
          {{ project.description.substring(0, 200) }}
          <span v-if="project.description.length > 200">...</span>
        </div>
      </v-card-text>

      <v-divider class="mx-4"></v-divider>

      <v-card-actions>
        <v-btn color="deep-purple lighten-2" text @click="dialog = true">
          Read More
        </v-btn>
        <v-spacer></v-spacer>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              v-if="project.repo"
              :href="project.repo"
              target="_blank"
              v-bind="attrs"
              v-on="on"
              depressed
              fab
              ><v-icon>mdi-github</v-icon></v-btn
            >
          </template>
          <span>Visit github Repo</span>
        </v-tooltip>
        <div style="width: 10px"></div>
        <v-tooltip bottom>
          <template v-slot:activator="{ on, attrs }">
            <v-btn
              v-if="project.launch"
              :href="project.launch"
              target="_blank"
              v-bind="attrs"
              v-on="on"
              depressed
              fab
              ><v-icon color="deep-purple lighten-2">
                mdi-rocket-launch</v-icon
              ></v-btn
            >
          </template>
          <span>Launch Application</span>
        </v-tooltip>
      </v-card-actions>
    </v-card>
    <v-dialog transition="dialog-top-transition" v-model="dialog" width="1200">
      <v-card>
        <v-card-title class="text-h5 grey lighten-2">
          {{ project.title }}
        </v-card-title>

        <v-card-text>
          <v-carousel hide-delimiters v-model="model">
            <v-carousel-item v-for="(pic, i) in project.pics" :key="i">
              <div class="carol">
                <img :src="pic" alt="" height="500" />
              </div>
            </v-carousel-item>
          </v-carousel>
          <p class="p-5">{{ project.description }}</p>
          <ul>
            <li v-for="(tech, index) in project.technologies" :key="index">
              {{ tech }}
            </li>
          </ul>
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-btn text color="deep-purple lighten-2" @click="dialog = false"
            >close</v-btn
          >
          <v-spacer></v-spacer>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                v-if="project.repo"
                :href="project.repo"
                target="_blank"
                v-bind="attrs"
                v-on="on"
                depressed
                fab
                ><v-icon>mdi-github</v-icon></v-btn
              >
            </template>
            <span>Visit github Repo</span>
          </v-tooltip>
          <div style="width: 10px"></div>
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                v-if="project.launch"
                :href="project.launch"
                target="_blank"
                v-bind="attrs"
                v-on="on"
                depressed
                fab
                ><v-icon color="deep-purple lighten-2">
                  mdi-rocket-launch</v-icon
                ></v-btn
              >
            </template>
            <span>Launch Application</span>
          </v-tooltip>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
export default {
  props: ["project"],
  data: () => ({
    loading: false,
    selection: 1,
    dialog: false,
    model: 0,
  }),
};
</script>

<style scoped>
.carol {
  width: 100%;
  display: flex;
  justify-content: center;
}
</style>
