<template>
  <Layout>

    <!-- Learn how to use images here: https://gridsome.org/docs/images 
    <g-image alt="Example image" src="~/favicon.png" width="135" /> -->

    <div class="jumbotron Hero text-center">
  <h1 class="display-4">Witam na mojej stronie.</h1>
  <p class="lead">Studiuję Informatykę w Państwowej Wyższej Szkole Zawodowej w Legnicy.</p>
  <hr class="my-4">
  <p class="lead">
    <a class="btn btn-primary btn-lg" href="#works" role="button">Moje prace</a>
  </p>
</div>

    <div class="Portfolioworks container" id="works">
      <h2>Moje prace</h2>
      <p>Łącznie: {{ $page.allWork.totalCount}}</p>

         <div class="row">
        <div class="Work col-md-6" v-for="work in $page.allWork.edges" :key="work.node.id">
          <g-link :to="work.node.path">
            <div class="WorkCard">
              <g-image v-if="work.node.image != null" :src="work.node.image.src"></g-image>
          <h2 class="WorkTitle">{{ work.node.title }}</h2>
          <p>{{ work.node.description }}</p>
          </div>
          </g-link>
          </div>

        </div>
        </div>

  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Strona główna'
  }
}
</script>

<page-query>
query {
	allWork {
    totalCount
    edges {
      node {
        id
        title
        description
        path
        content
        image (width: 470)
      }
    }
  }
}
</page-query>

<style>

.jumbotron {
  background-image: url(IMG_20190902_195348.jpg); background-size: cover;
   background-color: hsla(0,0%,100%,0.70);
    background-blend-mode: overlay;
    background-repeat: no-repeat;
}
.Hero {
  padding-top: 10rem;
  padding-bottom: 10rem;
}

.Work {
  padding: 2rem 2rem;
}

.WorkCard {
box-shadow: 0px 0px 20px rgba(0,0,0,0.1);
padding: 1rem;
border-radius: 0.2rem;
}

.Portfolioworks {
background: transparent;
color :black;
}
.home-links a {
  margin-right: 1rem;
}
</style>
