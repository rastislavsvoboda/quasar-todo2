<template>
  <q-page class="row">
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
      <q-list bordered="">
        <q-item>
          <q-item-section side="">
            <q-checkbox :model-value="true"> </q-checkbox>
          </q-item-section>
          <q-item-section> Go shopping </q-item-section>
          <q-item-section side="">
            <q-btn flat round size="small" icon="mdi-delete"></q-btn>
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>

    <div class="col-xs-3">
      <q-toolbar class="bg-primary">
        <q-btn
          fab
          icon="mdi-plus"
          color="secondary"
          style="margin-bottom: -42px"
          class="q-ml-md"
        >
        </q-btn>
      </q-toolbar>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  data() {
    return {
      selected: "",
      search: "",
    };
  },
});
</script>
