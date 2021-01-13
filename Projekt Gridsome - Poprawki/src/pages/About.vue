<template>
<v-container>
    <v-row>
      <v-col>
        <section id="o-mnie">
    <div class="jumbotron text-center">
  <p class="display-4">O mnie</p>
  <p class="lead">Grafik i fotograf amator, entuzjastka psychologii, diagnosta własnego samochodu i licznych komputerów, kolekcjonerka. Fanka gier RPG.</p>
  <p class="lead">Przyszła inżynier informatyki.</p>
  <hr class="my-4">
         </div> 
</section> 
      </v-col>
    </v-row>

    <v-row justify="space-around" class="mb-lg-16">
      <v-card width="700" color="transparent">
            <v-spacer></v-spacer>

          <v-card-title class="">
            <p class="ml-8">
              Edukacja
            </p>
          </v-card-title>

        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">
            Dziś
          </div>

          <v-timeline
            align-top
            dense
          >
            <v-timeline-item
              v-for="message in messages"
              :key="message.time"
              :color="message.color"
              small
            >
              <div>
                <div class="font-weight-normal">
                  <strong>{{ message.from }}</strong>, {{message.time}}
                </div>
                <div>{{ message.message }}</div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card>

      <v-card width="700" color="transparent">
            <v-spacer></v-spacer>

          <v-card-title class="">
            <p class="ml-8">
              Kompetencje
            </p>
          </v-card-title>

        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2">
          </div>

          <v-timeline
            align-top
            dense
          >
            <v-timeline-item
              v-for="ability in abilities"
              :key="ability.time"
              :color="ability.color"
              small
            >
              <div>
                <div class="font-weight-normal">
                  <strong>{{ ability.description }}</strong>
                </div>
                <div>{{ ability.info }}</div>
              </div>
            </v-timeline-item>
          </v-timeline>
        </v-card-text>
      </v-card>
    </v-row>
    <section>
      <br>
       <p class="lead text-center">W wolnym czasie zajmuję się pisaniem tekstów lub opowiadań,
        a także intensywnym eksperymentowaniem na podzespołach laptopa celem osiągnięcia wyższej wydajności 
        <br>(w tym czynności takie jak undervolting i overclocking).</p>
        <hr class="my-4">

</section> 
  </v-container>
</template>

<script>
export default {
      data: () => ({
      messages: [
        {
          from: 'Państwowa Wyższa Szkoła Zawodowa im. Witelona w Legnicy',
          message: 'Informatyka (Grafika komputerowa)',
          time: '10.2018 - obecnie',
          color: 'deep-purple',
        },
        {
          from: 'I Liceum Ogólnokształcące im. ks. Bolka I w Jaworze',
          message: 'Profil matematyczno-fizyczny',
          time: '09.2015 - 04.2018',
          color: 'blue',
        },
      ],
      abilities: [
        {
          description:'Znajomość języka angielskiego (ogólna)',
          info:'Poziom: C1',
          color:'red darken-1',
        },
        {
          description:'Znajomość języka angielskiego (w biznesie)',
          info:'Poziom: B2',
          color:'red',
        },
        {
          description:'Znajomość programu Adobe Photoshop',
          info:'Poziom: Średni',
          color:'orange darken-1',
        }
      ]
    }),

}
</script>
