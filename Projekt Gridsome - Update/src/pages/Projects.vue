<template>
<v-container id="projekty">
    <v-row>
      <v-col>
       <div class="jumbotron text-center">
          <p class="display-3">Projekty</p>
        </div>
      </v-col>
    </v-row>
    <v-row class="justify-center">
  <v-card
    v-for="project in projects"
    :key="project.name"
    class="mx-lg-6 my-lg-6"
    max-width="400"

  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src="project.image"
    >

    </v-img>

    <v-card-subtitle class="text--primary">
      {{project.name}}
    </v-card-subtitle>
     <v-card-text class="pb-0">
      <div>{{project.description}}</div>

      <div>{{project.year}}</div>
    </v-card-text>
    <v-card-actions>
      <v-btn
        color="black"
        text
        :href="project.github"
      >
        Podgląd
      </v-btn>

    </v-card-actions>
  </v-card>
        </v-row>
      </v-container>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          name: 'Tekstura własna (grassy)',
          description: 'Programowanie wizualne',
          year: '2020',
          github: 'https://github.com/Ristie/sm-s3gk/blob/d9a0a6399d207280efcbeaaad368b9466cfcbad8/grassy.png',
          image:'https://raw.githubusercontent.com/Ristie/sm-s3gk/d9a0a6399d207280efcbeaaad368b9466cfcbad8/grassy.png'
        },
        {
          name: 'Tekstura własna (tex)',
          description: 'Programowanie wizualne',
          year: '2020',
          github: 'https://github.com/Ristie/sm-s3gk/blob/0f9934274d35524cf72bf7f74c9fe51fbc34bd7b/tex.png',
          image:'https://raw.githubusercontent.com/Ristie/sm-s3gk/0f9934274d35524cf72bf7f74c9fe51fbc34bd7b/tex.png'
        },
        {
          name: 'Tekstura własna (neon)',
          description: 'Programowanie wizualne',
          year: '2020',
          github: 'https://github.com/Ristie/sm-s3gk/blob/0f9934274d35524cf72bf7f74c9fe51fbc34bd7b/neon.png',
          image:'https://raw.githubusercontent.com/Ristie/sm-s3gk/0f9934274d35524cf72bf7f74c9fe51fbc34bd7b/neon.png'
        },
        {
          name: 'Tło dla okładki płyty',
          description: 'Programy graficzne i DTP',
          year: '2021',
          github: 'https://github.com/Ristie/sm-s3gk/blob/master/okladka126x126.jpg',
          image: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/master/okladka126x126.jpg'
        },
        {
          name: 'Wizualny prototyp strony',
          description: 'Zaawansowane metody grafiki komputerowej',
          year: '2020',
          github: 'https://github.com/Ristie/sm-s3gk/blob/master/projekt_strony_cz1.jpg',
          image: 'https://raw.githubusercontent.com/Ristie/sm-s3gk/master/projekt_strony_cz1.jpg',
        }
      ]
    }
  },
  
}
</script>
