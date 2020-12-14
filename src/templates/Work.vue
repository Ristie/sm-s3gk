<template>
<Layout>
    <div class="jumbotron text-center">
<h1>{{$page.work.title}}</h1>
<h6 class="display-6">{{$page.work.description}}</h6>
<hr class="my-4">
  <g-image v-if="$page.work.image != null" :src="$page.work.image.src"></g-image>
<hr class="my-4">
<a class="btn btn-primary btn-lg" href="#description" role="button">Szczegóły</a>
</div>
<div class="container" id="description">
    <div class="row">
    <div class="col-8 offset-2" v-html="$page.work.content"></div>
    </div>
    </div>
</Layout>
</template>

<style>

</style>

<script>
export default {
  metaInfo: {
    title: 'Praca'
  }
}
</script>


<page-query>
query Works ($path: String) {
  work:work(path: $path) {
    title
    description
    content
    image (width: 1080)
  }
}
</page-query>