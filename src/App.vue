<template>
  <div id="app">
    <form>
          <label for ="firstname">
              First Name: <input id="firstname" type="text" v-model="firstName" placeholder="Enter your firstname">
          </label> 
      <br>
          <label for="lastname">
              Last Name: <input id="lastname" type="text" v-model="lastname" placeholder=" Enter your lastname">
          </label>
      <br>

      <button @click.prevent="submitForm"> FullName </button>

        <p v-if="isSubmitted"> Your full name is {{ fullName = firstName + " " + lastName }} </p>
    </form>
  </div>
</template>

<script>



export default {
  name: 'App',
  data() {
    return {
      firstName: "",
      lastName: "",
      fullName: null,
      isSubmitted: false
    }
  },

  methods: {
    submitForm() {
      this.isSubmitted = true;
    }
  }

}  
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
