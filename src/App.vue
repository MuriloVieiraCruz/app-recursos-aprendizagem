<template>
    <ul>
        <learning-resources 
        v-for="res in storedResources" 
        :key="res.id"
        :title="res.title"
        :description="res.description"
        :link="res.link"
        ></learning-resources>
    </ul>
</template>

<script>
import LearningResource from './components/learning-resources/LearningResource.vue';

export default {
    components: {
        'learning-resources': LearningResource
    },
    data() {
        return {
            storedResources: [
                {
                    id: 'official-guide',
                    title: 'Official Guide',
                    description: 'The official Vue.js documentation',
                    link: 'https://vuejs.org'
                },
                {
                    id: 'google',
                    title: 'Official Google',
                    description: 'The official Google',
                    link: 'https://google.com'
                }
            ]
        }
    }
}
</script>