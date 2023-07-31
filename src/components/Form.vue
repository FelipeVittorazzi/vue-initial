<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div id="app">
    <form @submit.prevent="onSubmit">
      <div>
        <label for="name">Nome:</label>
        <input id="name" v-model="name" type="text">
      </div>
      <div>
        <label for="number">Número:</label>
        <input id="number" v-model="number" type="text">
      </div>
      <div>
        <label for="email">Email:</label>
        <input id="email" v-model="email" type="text">
      </div>
      <div>
        <label for="cpf">CPF:</label>
        <input id="cpf" v-model="cpf" type="text">
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: '',
      number: '',
      email: '',
      cpf: ''
    }
  },
  methods: {
    onSubmit () {
      // process form
      console.log('Form Submitted: ', this.name, this.number, this.email, this.cpf);
    }
  }
}
</script>
