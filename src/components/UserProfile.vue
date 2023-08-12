<template>
    <section class="user-profile">
      <div class="user-info">
        <div class="avatar">
          <img :src="user.avatar_url" alt="User Avatar">
        </div>
        <div class="details">
          <h1>{{ user.name }}</h1>
          <h2>@{{ user.username }}</h2>
          <p>{{ user.bio }}</p>
          <div class="stats">
            <span class="followers">Followers: {{ user.followers }}</span>
            <span class="following">Following: {{ user.following }}</span>
          </div>
        </div>
      </div>
      <h2>Repositories</h2>
      <ul class="repository-list">
        <li v-for="(repo, index) in repositories" :key="index">
          <h3>{{ repo.name }}</h3>
          <p>{{ repo.description }}</p>
        </li>
      </ul>
    </section>
  </template>

<script>
export default {
  props: {
    user: Object, // Passed in from parent component
    repositories: Array // Passed in from parent component
  }
};
</script>

<style scoped>
.user-profile {
  margin-top: 20px;
  padding: 20px;
  border: 1px solid #ccc;
  background-color: #f9f9f9;
}

.user-info {
  display: flex;
  align-items: center;
}

.avatar img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin-right: 20px;
}

.details h1 {
  font-size: 1.5rem;
  margin-bottom: 5px;
}

.details h2 {
  color: #555;
  font-size: 1.2rem;
  margin-bottom: 10px;
}

.stats {
  margin-top: 10px;
}

.repository-list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.repository-list li {
  margin-bottom: 15px;
}

.repository-list h3 {
  font-size: 1.2rem;
  margin-bottom: 5px;
}

.repository-list p {
  color: #555;
}
</style>
