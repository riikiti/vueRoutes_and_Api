<template class="Jobs">
  <h2>All Jobs</h2>
  <div v-for="job in jobs" :key="job.id" class="job">
    <router-link :to="{ name: 'JobsDetails',params:{id:job.id}}">
      <h2>{{ job.title }}</h2></router-link
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      jobs: [
        { title: "Number one", id: 1, description: "kurwa1" },
        { title: "Number two", id: 2, description: "kurwa2" },
        { title: "Number three", id: 3, description: "kurwa3" },
      ],
    };
  },
};
</script>

<style>
</style>