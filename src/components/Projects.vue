<template>
    <div>
        <h1>Projects</h1>
        <p>These are some of my projects, you can find all of them on my
            <a class="no-underline" href="https://github.com/Panda-ManR" target="_blank">
            <v-hover>
                <font-awesome-icon :icon="['fab', 'github']" @mouseover="next_active = true" @mouseout="next_active = false"
                                   slot-scope="{ hover }"
                                   :class="`${hover? 'icon-active': 'icon-inactive'}`"/>
            </v-hover>
            </a>
        </p>
        <div class="projects">
            <Project v-for="item in projects"
                          v-bind:name="item.name"
                          v-bind:url="item.url"
                          v-bind:description="item.description"
                          v-bind:src="item.src"
                          v-bind:tags="item.tags"
                          v-bind:key="item.id">
            </Project>
        </div>
    </div>
</template>

<script>
import Project from '@/components/Project.vue';
import { mapGetters, mapActions } from 'vuex';

export default {
    name: 'Home',
    components: {
        Project,
    },
    created() {
        this.fetchProjects();
    },
    computed: {
        ...mapGetters([
            'projects',
        ]),
    },
    methods: {
        ...mapActions([
            'fetchProjects',
        ]),
    },
};
</script>

<style scoped>

</style>
