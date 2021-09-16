<template>
  <q-page class="row page-bg">
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
          v-model="search"
          class="full-width"
          dense
          borderless
          placeholder="Search"
        >
          <template #append="">
            <q-icon name="mdi-magnify"></q-icon>
          </template>
        </q-input>
      </q-toolbar>
      <TodosList bordered="">

      </TodosList>
    </q-card>

    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <CreateTodoButton
          fab
          icon="mdi-plus"
          color="secondary"
          style="margin-bottom: -42px"
          class="q-ml-md"
        >
        </CreateTodoButton>
      </q-toolbar>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import { colors } from "quasar";
import CreateTodoButton from "components/CreateTodoButton.vue"
import TodosList from "components/TodosList.vue"
const { getPaletteColor } = colors;

export default defineComponent({
  name: "PageIndex",
    components: {
      CreateTodoButton,
      TodosList
    },
  data() {
    return {
      selected: "",
      search: "",
    };
  },
  mounted() {
    console.log(getPaletteColor("blue-9"));
  },
});
</script>

<style lang="scss">
.page-bg {
  background-color: $primary;
}
</style>
