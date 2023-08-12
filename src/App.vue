<template>
  <div class="app">
    <AppHeader />
    <AppBanner />
    <RepositoriesGrid />
    <RepositoryDetail/>
    <UserProfile/>
    <ExploreSection/>
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader.vue";
import AppBanner from "@/components/AppBanner.vue";
import RepositoriesGrid from "@/components/RepositoriesGrid.vue";
import RepositoryDetail from "./components/RepositoryDetail.vue";
import UserProfile from "./components/UserProfile.vue";
import ExploreSection from "./components/ExploreSection.vue";
import AppFooter from "@/components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    AppBanner,
    RepositoriesGrid,
    RepositoryDetail,
    UserProfile,
    ExploreSection,
    AppFooter,
  },
};
</script>

<style>
/* Basic styling for the app container */
.app {
  font-family: Arial, sans-serif;
  background-color: #f7f7f7;
  color: #333;
  /* Add more styles as needed */
}
</style>
