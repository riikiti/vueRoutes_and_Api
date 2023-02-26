<template class="Jobs">
  <div v-if="job">
    <h2>{{ job.title }}</h2>
    <p>{{ job.description }}</p>
  </div>
  <div v-else>
    <h2>loading...</h2>
  </div>
</template>
  
  <script>
export default {
  props: ["id"],
  data() {
    return {
      job: null,
    };
  },
  mounted() {
    fetch("http://localhost:3000/jobs/" + this.id)
      .then((res) => res.json())
      .then((data) => (this.job = data))
      .catch((err) => console.log(err));
  },
};
</script>
  
  <style>
</style>