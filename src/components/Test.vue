<template>
  <form id="test">
    <div v-if="errors.length">
      <b>Please correct the following error(s):</b>
      <ul>
        <li v-for="error in errors" :key="error.id">{{ error }}</li>
      </ul>
    </div>

    <p>
      <label for="name">Name</label>
      <input type="text" name="name" id="name" v-model="thisName">
    </p>

    <p>
      <label for="email">Email</label>
      <input id="email" v-model="thisEmail" type="email" name="email" @change="$emit('setData',thisEmail)">
    </p>

    <p>
        <b-button @click="checkForm">Submit</b-button>
    </p>
    {{name}}{{email}}
  </form>
</template>

<script>
export default {
  name: "test",
  data() {
    return {
      errors: [],
      thisName: this.name,
      thisEmail: this.email
    };
  },
  props: ["name", "question", 'email'],
  methods: {
    checkForm: function(e) {
      if (this.thisName) return this.$router.push('/');
      this.errors = [];
      if (!this.thisName) this.errors.push("Name required.");
      e.preventDefault();
    }
  }
};
</script>
