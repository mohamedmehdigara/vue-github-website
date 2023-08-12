<template>
    <div>
      <!-- Other content -->
      <RepositoryDetail :repository="selectedRepository" :commits="recentCommits" />
      <!-- Other content -->
    </div>
  </template>
  
  <script>
  import RepositoryDetail from "@/components/RepositoryDetail.vue";
  
  export default {
    components: {
      RepositoryDetail,
    },
    data() {
      return {
        selectedRepository: {
          name: "My Repository",
          description: "A description of my repository",
          language: "JavaScript",
          stargazers_count: 100,
          forks_count: 50,
        },
        recentCommits: [
          {
            message: "Commit message 1",
            date: "2023-08-01",
          },
          {
            message: "Commit message 2",
            date: "2023-08-02",
          },
        ],
      };
    },
    mounted() {
      console.log("selectedRepository:", this.selectedRepository);
      console.log("recentCommits:", this.recentCommits);
    },
  };
  </script>
    
<style scoped>
.repository-detail {
  margin-top: 20px;
  padding: 20px;
  border: 1px solid #ccc;
  background-color: #f9f9f9;
}

.repository-detail h1 {
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.repository-detail p {
  margin-bottom: 15px;
}

.stats {
  margin-top: 10px;
}

.language {
  background-color: #007bff;
  color: white;
  padding: 2px 5px;
  border-radius: 3px;
  margin-right: 10px;
}

.commit-list {
  list-style: none;
  margin: 0;
  padding: 0;
}

.commit-list li {
  margin-bottom: 10px;
}

.commit-date {
  color: #777;
  font-size: 0.9rem;
  margin-left: 10px;
}
</style>
