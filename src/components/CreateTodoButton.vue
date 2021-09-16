<template>
  <q-btn @click="handleButtonClicked"/>
</template>

<script>
export default {
  name: 'CreateTodoButton',
  setup() {
    return {};
  },
  methods: {
    handleButtonClicked() {
      this.$q.dialog({
        title: 'Create Todo',
        prompt: {
          model: '',
          type: 'text'
        }
      }).onOk(this.createTodo)
    },
    createTodo(data) {
      console.log(data);
      this.$q.notify({
        message: 'Todo created',
        icon: 'mdi-check',
        color: 'positive'
      })
    }
  }
};
</script>
