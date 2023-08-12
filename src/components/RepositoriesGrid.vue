<template>
    <section class="repositories-grid">
      <div class="repository" v-for="(repo, index) in repositories" :key="index">
        <div class="repository-avatar">
        </div>
        <div class="repository-details">
          <h3>{{ repo.name }}</h3>
          <p>{{ repo.description }}</p>
          <div class="stats">
            <span class="stars">Stars: {{ repo.stargazers_count }}</span>
            <span class="forks">Forks: {{ repo.forks_count }}</span>
          </div>
        </div>
      </div>
      <button class="load-more" @click="loadMore">Load More</button>
    </section>
  </template>

<script>
export default {
  data() {
    return {
      repositories: [
        // Sample repository objects
        {
          name: 'Repo 1',
          description: 'Sample repository 1',
          stargazers_count: 10,
          forks_count: 5,
         
        },
        {
          name: 'Repo 2',
          description: 'Sample repository 2',
          stargazers_count: 20,
          forks_count: 8,
         
        },
        // ... add more repositories
      ]
    };
  },
  methods: {
    loadMore() {
      // Implement pagination or infinite scrolling logic here
    }
  }
};
</script>
<style scoped>
.repositories-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  grid-gap: 20px;
  margin-top: 20px;
}

.repository {
  border: 1px solid #ccc;
  padding: 20px;
  display: flex;
  align-items: center;
}

.repository-avatar img {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  margin-right: 15px;
}

.repository-details h3 {
  margin: 0;
}

.stats {
  margin-top: 10px;
}

.load-more {
  margin-top: 20px;
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  font-size: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.load-more:hover {
  background-color: #0056b3;
}
</style>
