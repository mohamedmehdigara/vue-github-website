<template>
    <footer class="footer">
      <div class="footer-links">
        <ul>
          <li><a href="#">Home</a></li>
          <li><a href="#">About</a></li>
          <li><a href="#">Blog</a></li>
          <!-- Add more links as needed -->
        </ul>
      </div>
      <div class="social-icons">
        <a href="#" class="icon"><i class="fab fa-facebook"></i></a>
        <a href="#" class="icon"><i class="fab fa-twitter"></i></a>
        <a href="#" class="icon"><i class="fab fa-instagram"></i></a>
        <!-- Add more social icons as needed -->
      </div>
      <div class="copyright">
        &copy; 2023 Your Website. All rights reserved.
      </div>
    </footer>
  </template>

<style scoped>
.footer {
  background-color: #333;
  color: white;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.footer-links ul {
  list-style: none;
  display: flex;
  padding: 0;
  margin: 0;
}

.footer-links li {
  margin-right: 20px;
}

.footer-links a {
  color: white;
  text-decoration: none;
}

.social-icons a.icon {
  color: white;
  font-size: 1.5rem;
  margin-right: 15px;
}

.social-icons a.icon:last-child {
  margin-right: 0;
}

.copyright {
  font-size: 0.8rem;
}
</style>

<script>
export default {
  name: 'AppFooter', // Update the component name
  // ... other component properties
};
</script>
