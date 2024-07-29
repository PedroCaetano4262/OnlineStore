<template>
  <div class="navbar">
    <ul class="navbar-left">
      <li><a class="active" href="#home">Home</a></li>
      <li><a href="#news">Products</a></li>
      <li><a href="#contact">Search</a></li>
    </ul>
    <ul class="navbar-right">
      <li><a href="javascript:void(0);" @click="toggleLogin">Login</a></li>
      <li><a href="javascript:void(0);" @click="toggleRegister">Sign Up</a></li>
    </ul>
  </div>

  <div class="container" v-if="isLogininvisible">
    <div class="overlay-container">
      <div class="overlay">
        <button class="close-btn" @click="toggleLogin">&times;</button>
        <h1>Login</h1>

        <label for="username">Username</label>
        <input type="text" placeholder="Enter Username" name="username" required>

        <label for="upassword">Password</label>
        <input type="password" placeholder="Enter Password" name="upassword" required>


      </div>
    </div>
  </div>

  <div class="container" v-if="isRegisterinvisible">
    <div class="overlay-container">
      <div class="overlay">
        <button class="close-btn" @click="toggleRegister">&times;</button>
        <h1>Register</h1>

        <label for="fname">First Name</label>
        <input type="text" placeholder="First Name" name="fname" required>

        <label for="lname">Last Name</label>
        <input type="text" placeholder="Last Name" name="lname" required>

        <label for="email">email</label>
        <input type="text" placeholder="Email" name="email" required>

        <label for="rpassword">Password</label>
        <input type="password" placeholder="Enter Password" name="rpassword" required>

        <label for="checkpassword">Confirm Password</label>
        <input type="password" placeholder="Confirm Password" name="checkpassword" required>


      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isLogininvisible: false,
      isRegisterinvisible: false
    };
  },
  methods: {
    toggleLogin() {
      this.isLogininvisible = !this.isLogininvisible;
      if(this.isRegisterinvisible == true){
        this.isRegisterinvisible = false;
      }
    },
    toggleRegister(){
      this.isRegisterinvisible = !this.isRegisterinvisible;
      if(this.isLogininvisible == true){
        this.isLogininvisible = false;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .container {
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  width: 100%;
  margin:auto;
}

.overlay-container {
  position: relative;
  background-color: white;
  padding: 15%;
  border-radius: 8px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
  width: 300px;
  max-width: 90%;
}

  .close-btn {
  position: absolute;
  top:0;
  right:0;
  background: none;
  border: none;
  font-size: 150%;
  font-weight: bold;
  color: darkslategray;
  cursor: pointer;
}

h1 {
  margin: 10%;
  text-align: center;
}

label {
  display: block;
  margin-bottom: 10%;
  font-weight: bold;
}

input[type="text"], input[type="password"] {
  width: 100%;
  padding: 10px;
  margin-bottom: 5%;
  border: 2px solid #ddd;
  box-sizing: border-box;
}
  .navbar {
    display: flex;
    justify-content: space-between; /* Distributes space between elements */
    align-items: center; /* Aligns items vertically */
  }

  .navbar-left {
    flex-grow: 1; /* Takes up remaining space */
  } 

  .navbar-right {
    margin-left: auto; /* Pushes items to the right */
  }
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: transparent;
  }
  li {
    float: left;
  }

  li a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
  }

  li a:hover{
    background-color: #E99330;
    font-weight: bold;
  }
</style>
