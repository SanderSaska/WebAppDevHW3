<template>
    <section class="Content">
        <aside class="Aside">
        </aside>
        <main class="Main" id="main">
            <article class="Article" v-for="post in postsList" :key="post.id">
                <section class="UserDate">
                    <img class="user_icon" v-bind:src="post.username_source" width="25" height="25" alt="User icon">
                    <p>{{post.username}}&ensp;&ensp;&ensp;</p>
                    <p>{{post.date}}</p>
                </section>
                <img v-bind:src="post.img_source" width="200" height="200">
                <p>{{post.description}}</p>
                <section class="Likes">
                    <button v-on:click="AddLike(post)">Like</button>
                    <p>{{post.likes}}</p>
                </section>
            </article>
        </main>
        <aside class="Aside">

        </aside>
    </section>
</template>

<script>
export default {
    name: "Post",
    data: function() {
        return {
        }
    },
computed: {
    postsList(){
        return this.$store.state.postsList
    }
},
methods: {
    AddLike(post){
        post.likes += 1;
    }
}
}
</script>

<style scoped>
* {
    font-family: 'Courier New', Courier, monospace;
}

p {
    line-height: 1.25;
}

::placeholder {
    color: grey;
}

</style>