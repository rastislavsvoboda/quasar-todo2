<template>
  <q-layout view="hHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          aria-label="Menu"
          flat
          dense
          round
          icon="mdi-menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Quasar App </q-toolbar-title>

        <div>
          <q-btn flat round icon="mdi-logout"></q-btn>
        </div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-toolbar class="bg-primary"> </q-toolbar>

      <q-item class="bg-grey-3">
        <q-item-section>Lists</q-item-section>
        <q-item-section side>
          <q-btn flat round size="sm" icon="mdi-plus" ></q-btn>
        </q-item-section>
      </q-item>

      <q-list>
        <q-item clickable>
          <q-item-section side>
            <q-icon name="mdi-shopping" color="red"></q-icon>
          </q-item-section>
          <q-item-section class="text-grey-9">Shopping List</q-item-section>
          <q-item-section side> 12 </q-item-section>
        </q-item>
      </q-list>
    </q-drawer>

    <q-page-container> <router-view> </router-view></q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {},

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
