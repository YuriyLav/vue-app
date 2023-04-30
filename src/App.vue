<template>
    <div class="app">
        <post-form  @create="createPost"/>
        <post-list v-bind:posts="posts"/>
    </div>
</template>

<script>
import PostForm from './components/PostForm.vue'
import PostList from '@/components/PostList.vue'

export default {
    components: {
        PostForm, PostList
    },
    data() {
        return {
            posts: [
                { id: 1, title: 'Javascript1', body: 'Опсиание поста1' },
                { id: 2, title: 'Javascript2', body: 'Опсиание поста2' },
                { id: 3, title: 'Javascript3', body: 'Опсиание поста3' },
                { id: 4, title: 'Javascript4', body: 'Опсиание поста4' },
            ],
        }
    },
    methods: {
        createPost(post) {
            this.posts.push(post)
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

.app {
    padding: 20px;
}

</style>