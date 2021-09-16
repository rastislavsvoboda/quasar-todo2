<template>
  <q-btn @click="handleButtonClicked"></q-btn>
</template>

<script>
export default {
  name: 'CreateTodoListButton',
  setup () {
    return {}
  },
  methods: {
    handleButtonClicked() {
      alert('click')
    }
  }
}
</script>
