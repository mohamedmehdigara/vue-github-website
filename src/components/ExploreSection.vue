<template>
    <section class="explore">
      <h1>Explore Repositories</h1>
      <div class="filters">
        <label for="category">Category:</label>
        <select id="category" v-model="selectedCategory">
          <option value="trending">Trending</option>
          <option value="popular">Popular</option>
          <!-- Add more options as needed -->
        </select>
        
        <label for="filter">Filter:</label>
        <input id="filter" v-model="filterText" placeholder="Filter by name">
        
        <label for="sort">Sort by:</label>
        <select id="sort" v-model="selectedSort">
          <option value="stars">Stars</option>
          <option value="forks">Forks</option>
          <!-- Add more options as needed -->
        </select>
      </div>
      
      <ul class="repository-list">
        <li v-for="(repo, index) in filteredRepositories" :key="index">
          <!-- Display repository information -->
        </li>
      </ul>
    </section>
  </template>

<script>
export default {
  name: 'ExploreSection',
  data() {
    return {
      repositories: [], // Fetch repositories from an API
      selectedCategory: 'trending',
      filterText: '',
      selectedSort: 'stars'
    };
  },
  computed: {
    filteredRepositories() {
      let filtered = this.repositories;

      // Apply filter by name
      if (this.filterText) {
        filtered = filtered.filter(repo => repo.name.toLowerCase().includes(this.filterText.toLowerCase()));
      }

      // Apply sort
      if (this.selectedSort === 'stars') {
        filtered.sort((a, b) => b.stargazers_count - a.stargazers_count);
      } else if (this.selectedSort === 'forks') {
        filtered.sort((a, b) => b.forks_count - a.forks_count);
      }

      return filtered;
    }
  }
};
</script>

<style scoped>
.explore {
  margin-top: 20px;
  padding: 20px;
  border: 1px solid #ccc;
  background-color: #f9f9f9;
}

.explore h1 {
  font-size: 1.5rem;
  margin-bottom: 20px;
}

.filters {
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 20px;
}

.filters label {
  margin-right: 10px;
}

.filters select, .filters input {
  padding: 5px;
  margin-right: 10px;
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

