<template>
<body class="blog-page">
  <header-layout>
  </header-layout>
    <h1>Blog</h1>
    <p v-for="post in $page.posts.edges" v-bind:key="post">
      <g-link :to="post.node.path">
        {{ post.node.title }}
      </g-link>
    </p>
    <footer-layout></footer-layout>
  </body>
</template>

<script>
export default {
  metaInfo: {
    title: 'Blog'
  }
}
</script>

<page-query>
query Posts {
  posts: allPost {
    edges {
      node {
        title
        path
      }
    }
  }
}
</page-query>

<style>
</style>