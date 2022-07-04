<template>
    <div class="about">
        <h1>This is a blog page</h1>
        <ul>
            <li v-for="post in posts">
                <h2>
                    <span>{{ post.id }}.&nbsp;</span>
                    <router-link :to="`/post/${post.id}`">{{ post.title }}</router-link>
                </h2>
                <p>{{ post.body }}</p>
            </li>
        </ul>
    </div>
</template>

<script>
import axios from "axios"
export default {
    name: 'Blog',
    data() {
        return {
            posts: []
        }
    },
    created() {
        const url = 'https://jsonplaceholder.typicode.com/'
        axios.get(url)
            .then(resp => {
                this.posts = resp.data
            })
            .catch(e => {
                console.log(e.response ? e.response.data : e)
            })


    }
}

</script>