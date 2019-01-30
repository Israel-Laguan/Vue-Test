<template>
  <div class="about">
    <h1>This is an about page</h1>
    <input v-model="message" placeholder="edit me">
<p>Message is: {{ message }}</p>
  </div>
</template>

<script>
export default {
  name:'About',
  data(){
    return{
      message:null
    }
  }
}
</script>
