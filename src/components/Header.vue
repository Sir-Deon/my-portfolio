<template>
  <v-container>
    <div class="header">
      <img
        class="animate__animated animate__bounce"
        src="/logo.png"
        alt=""
        height="100"
      />
      <v-btn
        color="#21B0F4"
        @click="dialog = true"
        rounded
        outlined
        class="mt-5"
      >
        Contact Me
      </v-btn>
    </div>
    <v-dialog
      transition="dialog-bottom-transition"
      v-model="dialog"
      width="500"
    >
      <v-card>
        <v-card-title color="#21b0f4" class="text-h5">
          Contact Me
        </v-card-title>

        <v-card-text>
          <v-icon color="#21b0f4">mdi-email</v-icon>
          deonachuo@gmail.com
          <br />
          <br />
          <v-icon color="#21b0f4">mdi-phone</v-icon>+237 651-788-492
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn text color="#21b0f4" @click="dialog = false">close</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script>
import "animate.css";
export default {
  data: () => ({
    dialog: false,
  }),
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
}
.v-btn {
  margin-top: 20px;
}

img {
  width: 15%;
}

@media screen and (max-width: 480px) {
  img {
    width: 30%;
    margin-top: -15px;
    margin-left: -20px;
  }
}
</style>
