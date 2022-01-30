<template>
  <form @submit.prevent="handleSubmit">
    <label>Name:</label>
    <input type="text" required v-model="name">

    <label>Address:</label>
    <input type="text" required v-model="address">

    <div class="submit">
      <button>Submit</button>
    </div>
  </form>
   <p>Name: {{ name }}</p>
   <p>Address: {{ address }}</p>
</template>

<script>
export default {
  data() {
    return {
      name: '',
      address: ''
    }
  },
  methods: {
    handleSubmit() {
      console.log("Form Submitted")
    }
  }
}
</script>

<style>
form {
  max-width: 420px;
  margin: 30px auto;
  background: white;
  text-align: left;
  padding: 40px;
  border-radius: 10px;
}
label {
  color: #aaa;
  display: inline-block;
  margin: 25px 0 15px;
  font-size: 0.6em;
  text-transform: uppercase;
  letter-spacing: 1px;
  font-weight: bold;
}
input {
  display: block;
  padding: 10px 6px;
  width: 100%;
  box-sizing: border-box;
  border: none;
  border-bottom: 1px solid #ddd;
  color: #555;
}
button {
  background: #0b6dff;
  border: 0;
  padding: 10px 20px;
  color: white;
  border-radius: 20px;
  margin-top: 20px;
}
.submit {
  text-align: center;
}
</style>