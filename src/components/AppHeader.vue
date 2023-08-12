<template>
    <header class="header">
      <nav class="navigation">
        <ul class="nav-list">
          <li><a href="#">Home</a></li>
          <li><a href="#">Explore</a></li>
          <li><a href="#">Features</a></li>
          <li><a href="#">Pricing</a></li>
          <li><a href="#">Blog</a></li>
          <li><a href="#">About</a></li>
        </ul>
      </nav>
      
      <div class="search-bar">
        <!-- Search input goes here -->
      </div>
      
      <div class="user-menu">
        <img class="user-avatar" src="path_to_avatar_image" alt="User Avatar">
        <div class="dropdown">
          <ul class="dropdown-list">
            <li><a href="#">Sign In</a></li>
            <li><a href="#">Sign Out</a></li>
            <li><a href="#">Profile</a></li>
          </ul>
        </div>
      </div>
    </header>
  </template>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;
  background-color: #333;
  color: white;
}

.navigation {
  display: flex;
  align-items: center;
}

.nav-list {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}

.nav-list li {
  margin-right: 20px;
}

.nav-list li a {
  color: white;
  text-decoration: none;
}

.search-bar {
  margin: 0 20px;
  flex-grow: 1;
  /* Style your search bar here */
}

.user-menu {
  display: flex;
  align-items: center;
}

.user-avatar {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 10px;
}

.dropdown {
  position: relative;
}

.dropdown-list {
  list-style: none;
  background-color: white;
  border: 1px solid #ccc;
  position: absolute;
  top: 100%;
  right: 0;
  display: none;
}

.user-menu:hover .dropdown-list {
  display: block;
}
</style>
<script>
export default {
  name: 'AppHeader', // Update the component name
  // ... other component properties
};
</script>

  