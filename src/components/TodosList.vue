<template>
  <q-list>
    <q-item>
      <q-item-section side="">
        <UpdateTodoCheckbox > </UpdateTodoCheckbox>
      </q-item-section>
      <q-item-section> Go shopping </q-item-section>
      <q-item-section side="">
        <DeleteTodoButton flat round size="small" icon="mdi-delete"></DeleteTodoButton>
      </q-item-section>
    </q-item>
  </q-list>
</template>

<script>
import UpdateTodoCheckbox from "components/UpdateTodoCheckbox.vue"
import DeleteTodoButton from "components/DeleteTodoButton.vue"
export default {
  name: 'TodosList',
  components: {
    UpdateTodoCheckbox,
    DeleteTodoButton,
  }
};
</script>
