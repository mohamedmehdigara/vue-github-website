<template>
    <section class="banner">
      <div class="banner-content">
        <h1>Join GitHub Today</h1>
        <p>Discover, collaborate, and build amazing things together.</p>
        <button class="cta-button">Get Started</button>
      </div>
    </section>
  </template>


<style scoped>
.banner {
  background-size: cover;
  background-position: center;
  height: 400px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
  text-align: center;
}

.banner-content {
  max-width: 800px;
  padding: 20px;
}

.banner-content h1 {
  font-size: 2.5rem;
  margin-bottom: 10px;
}

.banner-content p {
  font-size: 1.2rem;
  margin-bottom: 20px;
}

.cta-button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.cta-button:hover {
  background-color: #0056b3;
}
</style>

<script>
export default {
  name: 'AppBanner', // Update the component name
  // ... other component properties
};
</script>