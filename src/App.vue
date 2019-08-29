<template>
  <v-app>
    <v-app-bar dense app dark height=60>
      <v-toolbar-title class="headline text-uppercase">
        <span>Dakota </span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-divider vertical></v-divider>
      <v-btn
        text
        href="https://www.linkedin.com/in/dakota-parker-7a1041137/"
        target="_blank"
        style="margin-left:5px"
      >
        ADD ME ON
        <img src="@/assets/linkedin.svg" style="margin-left:5px;height:20px"/>
      </v-btn>
    </v-app-bar>

    <v-content style="background-color:rgb(33,33,33);height:calc(100vh - 60px)">
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data: () => ({
    //
  }),
};
</script>
