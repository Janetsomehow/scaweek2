<template>
  <div id="app">
    <form>
          <label for ="firstname">
              First Name: <input type="firstname"  v-model="firstName" placeholder="Enter your firstname">
          </label> <br>
    
          <label for="lastname">
              Last Name: <input type="lastname" v-model="lastname" placeholder=" Enter your lastname">
          </label>
      <br>

      <button @click.prevent="submitForm"> FullName </button>

        
    </form>
  </div>
</template>

<script>



export default {
  name: 'App',
  data() {
    return {
      firstName: "",
      lastName: ""
      
    }
  },

 computed: {
    fullName() {
  return `${this.firstName} ${this.lastName}`
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
