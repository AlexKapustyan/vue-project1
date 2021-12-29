<template>
  <div id="app" class="app">
    <!-- <h1>Vue learn 'Lesson 2'</h1> -->

    <h3 :title="posts[0].id">{{ posts[0].title }}</h3>

    <p v-if="condition">первое <br>{{ posts[0].body }}</p>
		<p v-else-if="!condition">второе <br>{{ posts[1].body }}</p>
		<p v-else>Иначе</p>

    <!-- <div v-for="(post, index) of 3" :key="index" class="post-item">
      {{ index + 1 }} {{ post.title }} -->

    <!-- <p v-for="(value, key, index) in post" :key="index" class="post-field">
        {{ key }}: {{ value }}
      </p> -->
    <!-- </div> -->
  </div>
</template>

<script>
export default {
  name: "App",
  data: () => ({
    posts: [
      {
        userId: 1,
        id: 1,
        title: "optio molestias id quia eum",
        body: "quo et expedita modi cum officia vel magni\ndolorib…it\nquos veniam quod sed accusamus veritatis error. Quo et expedita modi cum officia vel magni\ndolorib…it\nquos veniam quod sed accusamus veritatis error. Quo et expedita modi cum officia vel magni\ndolorib…it\nquos veniam quod sed accusamus veritatis error",
      },
      {
        userId: 1,
        id: 2,
        title: "qui est esse",
        body: "est rerum tempore vitae\nsequi sint nihil reprehend…aperiam non debitis possimus qui neque nisi nulla. Est rerum tempore vitae\nsequi sint nihil reprehend…aperiam non debitis possimus qui neque nisi nulla.  Est rerum tempore vitae\nsequi sint nihil reprehend…aperiam non debitis possimus qui neque nisi nulla.",
      },
      {
        userId: 2,
        id: 3,
        title: "ea molestias quasi exercitationem repellat qui ipsa sit aut",
        body: "et iusto sed quo iure\nvoluptatem occaecati omnis e…\nmolestiae porro eius odio et labore et velit aut. Ea molestias quasi exercitationem repellat qui ipsa sit aut. Et iusto sed quo iure\nvoluptatem occaecati omnis e…\nmolestiae porro eius odio et labore et velit aut. Ea molestias quasi exercitationem repellat qui ipsa sit aut. Et iusto sed quo iure\nvoluptatem occaecati omnis e…\nmolestiae porro eius odio et labore et velit aut.",
      },
      {
        userId: 2,
        id: 4,
        title: "eum et est occaecati",
        body: "ullam et saepe reiciendis voluptatem adipisci\nsit … ipsam iure\nquis sunt voluptatem rerum illo velit. Ullam et saepe reiciendis voluptatem adipisci\nsit … ipsam iure\nquis sunt voluptatem rerum illo velit. Ullam et saepe reiciendis voluptatem adipisci\nsit … ipsam iure\nquis sunt voluptatem rerum illo velit",
      },
      {
        userId: 3,
        id: 5,
        title: "nesciunt quas odio",
        body: "repudiandae veniam quaerat sunt sed\nalias aut fugi…sse voluptatibus quis\nest aut tenetur dolor neque. repudiandae veniam quaerat sunt sed\nalias aut fugi…sse voluptatibus quis\nest aut tenetur dolor neque. repudiandae veniam quaerat sunt sed\nalias aut fugi…sse voluptatibus quis\nest aut tenetur dolor neque",
      },
      {
        userId: 3,
        id: 6,
        title: "dolorem eum magni eos aperiam quia",
        body: "ut aspernatur corporis harum nihil quis provident …s\nvoluptate dolores velit et doloremque molestiae. Ut aspernatur corporis harum nihil quis provident …s\nvoluptate dolores velit et doloremque molestiae. Ut aspernatur corporis harum nihil quis provident …s\nvoluptate dolores velit et doloremque molestiae. Ut aspernatur corporis harum nihil quis provident …s\nvoluptate dolores velit et doloremque molestiae",
      },
      {
        userId: 4,
        id: 7,
        title: "magnam facilis autem",
        body: "dolore placeat quibusdam ea quo vitae\nmagni quis e…t excepturi ut quia\nsunt ut sequi eos ea sed quas. Dolore placeat quibusdam ea quo vitae\nmagni quis e…t excepturi ut quia\nsunt ut sequi eos ea sed quas. Dolore placeat quibusdam ea quo vitae\nmagni quis e…t excepturi ut quia\nsunt ut sequi eos ea sed quas. Dolore placeat quibusdam ea quo vitae\nmagni quis e…t excepturi ut quia\nsunt ut sequi eos ea sed quas",
      },
      {
        userId: 4,
        id: 8,
        title: "dolorem dolore est ipsam",
        body: "dignissimos aperiam dolorem qui eum\nfacilis quibus…\nipsam ut commodi dolor voluptatum modi aut vitae. Dignissimos aperiam dolorem qui eum\nfacilis quibus…\nipsam ut commodi dolor voluptatum modi aut vitae. Dignissimos aperiam dolorem qui eum\nfacilis quibus…\nipsam ut commodi dolor voluptatum modi aut vitae.",
      },
    ],
		condition: false,
  }),
  methods: {},
  computed: {
    slicedPost() {
      return this.posts.slice(0, 2);
    },
  },
  // computed: {
  //   // firstPost() {
  //   //   return this.postsList[0].body;
  //   // },
  //   firstPost: {
  //     get() {
  //       return this.postsList[0].body;
  //     },
  //     set(newValue) {
  //       return (this.postsList[0].body = newValue);
  //     },
  //   },
  //   bye() {
  //     console.log("bye");
  //     return "I am a cash";
  //   },
  // },
};
</script>

<style>
body {
  text-align: center;
  padding: 50px;
}
</style>
