<template>
  <form @submit.prevent ="alertUser">
    <legend>Hello lovely customers! Would you like to benefit from free soft cookies?</legend>
    <h5>Fill out this form quickly so as not to miss your chance</h5>
    <label>Full Name</label>
    <input type="text" placeholder="Enter your name" required>
    <label>Mail Address</label>
    <input type="email" placeholder="Enter your mail address" required>
    <label>Phone Number</label>
    <input type="number" placeholder="Enter your phone number" required>
    <button>Submit</button>
  </form>
</template>


<script setup>
function alertUser() {
  try {
  alert("Submitted with succés")
  throw new Error("Submission Failure")
  } catch(error) {
    console.error(error)
  }
}

</script>


<style scoped>
form {
  display: flex;
  flex-direction: column;
  background-color: #be6f3a;
  color: #FFFFFF;
  padding: 50px;
  border-radius: 10px;
  opacity: 0.95;
  width: 45%;
  margin: auto;
}
label {
  font-size: 1em;
  
}
input {
  border-radius: 5px;
  padding: 10px;
  margin: 5px 0px 20px 0px;
  border: none;
  font-family: "Montserrat Alternates", sans-serif;
  color: #000000;
}
input::placeholder {
  color: #000;
}
input:focus{
  background-color: #000000;
  color: #ffffff;
  outline: none;
}
button {
  border-radius: 5px;
  padding: 10px;
  margin: 5px 0px 20px 0px;
  border: none;
  color: #ffffff;
  background-color: #7e5133;
  font-weight: bolder;
  font-size: 1em;
  font-family: "Montserrat Alternates", sans-serif;
  cursor: pointer;
}

button:hover {
  color: #7e5133;
  background-color: #ffffff;
}
</style>
