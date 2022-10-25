<template lang="pug">
q-layout(view='lHh Lpr lFf')
  q-header(elevated)
    q-toolbar
      q-btn(flat dense round icon='menu' aria-label='Menu' @click='toggleLeftDrawer')
      q-toolbar-title Quasar App
      div Quasar v{{ $q.version }}
  q-drawer(v-model='leftDrawerOpen' show-if-above bordered)
    q-list
      q-item-label(header) Menu
      q-item(v-for="menu in menus" :to="menu.link")
        q-item-section(avatar)
          q-icon(name="link")
        q-item-section {{menu.title }}
  q-page-container
    router-view
</template>

<script setup>
import { ref } from "vue";

const leftDrawerOpen = ref(false);
const toggleLeftDrawer = () => {
  leftDrawerOpen.value = !leftDrawerOpen.value;
};

const menus = [
  { link: "/", title: "Home" },
  { link: "/about", title: "About" },
];
</script>

<style lang="scss" scoped></style>
