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
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-toolbar class="bg-primary"> </q-toolbar>

      <q-item class="bg-grey-3">
        <q-item-section>Lists</q-item-section>
        <q-item-section side>
          <CreateTodoListButton
            flat
            round
            size="sm"
            icon="mdi-plus"
          ></CreateTodoListButton>
        </q-item-section>
      </q-item>

      <TodoListsList />
    </q-drawer>

    <q-page-container> <router-view> </router-view></q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import CreateTodoListButton from "components/CreateTodoListButton.vue";
import TodoListsList from "components/TodoListsList.vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    CreateTodoListButton,
    TodoListsList,
  },

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
