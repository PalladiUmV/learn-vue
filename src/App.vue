<template>

	<div class="app">
		<post-form @create="createPost" />
		<post-list v-bind:posts="posts" />
	</div>

</template>


<script> 
import PostForm from './components/PostForm.vue'
import PostList from './components/PostList.vue'

export default {
	components: {
    PostForm,
    PostList,
},
	data() {
		return {
			posts: [
				{id: 1, title: 'JavaScript', body: 'Описание поста'},
				{id: 2, title: 'JavaScript', body: 'Описание поста 2'},
				{id: 3, title: 'JavaScript', body: 'Описание поста 3'},
				{id: 4, title: 'JavaScript', body: 'Описание поста 4'},
			],
		}
	},
	methods: {
		createPost(post) {
			this.posts.push(post);
		},
	}
}

</script>





<style>

* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
	font-family: 'Roboto';
	font-size: 15px;
}

.app {
	padding: 20px;
}

</style>