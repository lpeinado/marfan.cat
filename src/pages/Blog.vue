<template>
  <Layout>
    <header class="header blog-header">
      <h1>Blog de l'associació</h1>
      <p>Entrades disponibles al blog:</p>
    </header>
    <section class="posts">
      <post-list v-for="edge in $page.allPost.edges" :key="edge.node.id" :post="edge.node" />
    </section>
  </Layout>
</template>

<script>
import PostList from "@/components/PostList";
export default {
  components: {
    postList:PostList
  },
  metaInfo: {
    title: "A simple blog"
  }
};
</script>

<page-query>
query {
  metaData {
    siteName
    siteDescription
  }
  allPost {
    totalCount
    edges {
      node {
        id
        title
        timeToRead
        description
        date (format: "D MMMM YYYY")
        path
      }
    }

  }
}
</page-query>

<style scoped>
.layout {
  min-height: 100vh;
  border: 15px solid #fecd43;
  max-width: 760px;
  margin: 0 auto;
  padding-left: 20px;
  padding-right: 20px;
}
.blog-header{
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
}
.footer {
  padding-top: calc(30em / 4);
  text-align: center;
  font-size: 1em;
}
.link {
  border: 2px dashed #fecd43;
  padding: 7px;
  color: #333;
  text-decoration: none;
}

.header {
  font-family: "Stylish";
  font-size: 35px;
  text-align: center;
  line-height: 20px;
  padding: 0.7em;
}
.header h2 {
  font-weight: 200;
  font-size: 35px;
}
</style>