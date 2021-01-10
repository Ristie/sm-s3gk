<template>

<section id="fotografie">
  <v-container>
    <v-row>
      <v-col>
        <div class="jumbotron text-center">
          <p class="display-3">Fotografie</p>
        </div>
      </v-col>
    </v-row>
      <v-row class="justify-center">
        <v-card
        v-for="photo in photos"
    :key="photo.name"
    class="mx-lg-4 my-lg-4"
    max-width="400"
    max-height="400"
  >
    <v-img
    height="400px"
      :src="photo.link"
    ></v-img>
  </v-card>
  </v-row>
  </v-container>
</section>
</template>


<script>
export default {
  data() {
    return {
      photos: [
        {
          name: '1',
          link: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/26.jpg'
        },
        {
          name: '2',
          link: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20180807_152011.jpg'
        },
        {
          name:'3',
          link:'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200430_202945.jpg'
        },
        {
          name: '4',
          link:'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200606_203601.jpg'
        },
        {
          name: '5',
          link: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200607_133741.jpg'
        },
        {
          name: '6',
          link: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200725_162749.jpg'
        },
        {
          name: '7',
          link: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200730_202705.jpg'
        },
        {
          name: '8',
          link: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200530_211440.png?raw=true'
        },
        {
          name: '9',
          link: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200601_135633.jpg?raw=true'
        },
        {
          name: '10',
          link: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200607_133741.jpg?raw=true'
        },
        {
          name: '11',
          link: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200622_141449.jpg?raw=true'
        },
        {
          name: '12',
          link: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200704_173301.jpg?raw=true'
        },
        {
          name: '13',
          link: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/Zdj%C4%99cia/IMG_20200711_162003.jpg?raw=true'
        },
        {
          name: '14',
          link: 'https://github.com/Ristie/sm-s3gk/blob/master/Zdj%C4%99cia/IMG_20200829_183458.jpg?raw=true'
        },
        {
          name: '15',
          link: 'https://github.com/Ristie/sm-s3gk/blob/master/Zdj%C4%99cia/IMG_20201125_130420.jpg?raw=true'
        }
         ]
    }
  },
  
}
</script>