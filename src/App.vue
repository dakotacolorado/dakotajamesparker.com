<template>
  <v-app>
    <v-app-bar dense app dark height=60>
      <v-toolbar-title class="headline">
        <span>Dakota Parker</span>
        <v-divider vertical></v-divider>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
        <v-btn
          text
          href="https://www.linkedin.com/in/dakota-parker-7a1041137/"
          target="_blank"
          style="margin-left:5px"
        >
          <img src="@/assets/linkedin.svg" style="margin-left:5px;height:25px"/>
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-content style="height:calc(100vh - 60px)">
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
  }),
};
</script>
