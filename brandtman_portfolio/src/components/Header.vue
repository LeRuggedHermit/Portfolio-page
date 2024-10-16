<template>
    <header>
        <div class="logo-container">
        <img src="../assets/SB_LOGO.png" alt="Logo" />
      </div>
      <div class="nav-container">
        <nav>
          <ul class="nav-menu">
            <li><router-link to="/">Home</router-link></li>
            <li><a href="#lab">Lab</a></li>
            <li><a href="#about">My story</a></li>
            <li><router-link to="/about">CV</router-link></li>
          </ul>
        </nav>
      </div>
    </header>
</template>

<script>
export default{
    name: 'siteHeader',

}
</script>

<style scoped>

header {
  width: 100%;
  background-color: white;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  align-content: center;
  font-weight: 300;
}

.logo-container {
  height: 80%;
  display: flex;
  align-items: center;
  align-content: center;
  margin-left: 2rem;
}

.logo-container img {
  width: 48px;
}

.nav-container {
  margin-right: 4rem;
  font-size: 19.3px;
}

.nav-menu {
  list-style: none;
  padding: 0;
  display: flex;
  gap: 4vmin; /* Space between menu items */
}

.nav-menu li {
  position: relative;
  color: #08005a; /* Text color */
}

.nav-menu a {
  text-decoration: none;
  color: #08005a; /* Text color */
  padding: 5px 0; /* Space around the text */
  display: inline-block;
  position: relative;
}

/* Hover effect */
.nav-menu a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0;
  height: 2px; /* Thickness of the underline */
  background-color: #08005a; /* Color of the underline */
  transition: width 0.3s ease-in-out; /* Animation effect */
}

.nav-menu a:hover::after {
  width: 100%; /* Expand the underline */
}


/*MQ */

@media screen and (max-width: 400px) {
  .nav-container {
    position: fixed; /* Stick to the viewport */
    bottom: 0; /* Stick to the bottom */
    left: 0; /* Align it to the left */
    width: 100%; /* Full viewport width */
    background-color: white; /* Background color for visibility */
    padding: 1rem; /* Add some padding for breathing space */
    z-index: 1000; /* Ensure it's above all other content */
    margin: 0; /* Remove any margins */
    height: auto; /* Reset any height that could interfere */
    border: solid black 1px;
  }

  .nav-menu {
    gap: 10vmin; /* Space between menu items */
    justify-content: center; /* Center the menu items */
    padding: 0; /* Reset padding to avoid extra space */
    
    width: 90%;
    font-size: 14px;
  }

  .logo-container {
    display: none;
  }}
</style>