<template>
  <div class="navbar">
    <ul class="navbar-left">
      <li><a class="active" href="#home">Home</a></li>
      <li><a href="#news">Products</a></li>
      <li><a href="#contact">Search</a></li>
    </ul>
    <ul class="navbar-right">
      <li><a href="">Login</a></li>
      <li><a href="">Sign Up</a></li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

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
