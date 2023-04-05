<template>
  <v-app id="inspire">
    <v-app-bar class="px-3" color="white" flat density="compact">
      <v-toolbar-title>Title by Index.vue</v-toolbar-title>
      <v-tabs centered color="grey-darken-2" v-model="tab">
        <v-tab v-for="(link, i) in links" :key="i" :value="i">
          {{ link }}
        </v-tab>
      </v-tabs>
      <v-spacer></v-spacer>
    </v-app-bar>
    <v-main class="bg-grey-lighten-3">
      <v-window v-model="tab">
        <v-window-item
          transition="fade-transition"
          reverse-transition="fade-transition"
        >
          <HomeContent></HomeContent>
        </v-window-item>
        <v-window-item
          transition="fade-transition"
          reverse-transition="fade-transition"
        >
          <About></About>
        </v-window-item>
        <v-window-item
          transition="fade-transition"
          reverse-transition="fade-transition"
        >
          <Contact></Contact>
        </v-window-item>
      </v-window>
    </v-main>
    <v-footer class="bg-grey-lighten-1">
      <v-row justify="center" no-gutters>
        <v-btn
          v-for="(link, i) in links"
          :key="i"
          color="white"
          variant="text"
          class="mx-2"
          rounded="xl"
        >
          {{ link }}
        </v-btn>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
import HomeContent from "./contents/HomeContent.vue";
import About from "./contents/About.vue";
import Contact from "./contents/Contact.vue";

export default {
  components: {
    HomeContent,
    About,
    Contact,
  },
  data() {
    return {
      tab: 0,
      links: ["ホーム", "About", "Contact"],
    };
  },
};
</script>

<style>
.sheet {
  padding: 100px;
}
</style>
