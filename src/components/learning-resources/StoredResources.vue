<template>
    <ul>
        <learning-resources 
        v-for="res in resources" 
        :key="res.id"
        :title="res.title"
        :description="res.description"
        :link="res.link"
        ></learning-resources>
    </ul>
</template>

<script>
import LearningResource from './LearningResource.vue';

export default { 
    props: ['resources'],
    components: {
        'learning-resources': LearningResource
    },
}
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>