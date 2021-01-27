<template>
  <Layout>
    <div>
      <h1>{{$page.post.title}}</h1>
      <h5>{{$page.post.content}}</h5>
    </div>
  </Layout>
</template>

<page-query>
query($id: ID!) {
  post(id: $id) {
    id
    title 
    content
  }
}
</page-query>

<script>
export default {
  name: "PostPage",
  metaInfo() {
    return {
      title: this.$page.post.title
    }
  }
};
</script>
