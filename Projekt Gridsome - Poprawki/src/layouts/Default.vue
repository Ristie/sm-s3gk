<template>
  <v-app>
  

    <v-navigation-drawer color="rgba(255, 255, 255, 0.5)"  width="240px" permanent fixed>
      <v-list-item-avatar class="ml-lg-4">
              <v-img src="https://github.com/Ristie/sm-s3gk/blob/master/Zdj%C4%99cia/Snapchat-1176061906.jpg?raw=true"></v-img>
            </v-list-item-avatar>
      <v-list-item>
        
        <v-list-item-content>
          <v-list-item-title class="title">
            Emilia Szafarowska
          </v-list-item-title>
          <v-list-item-subtitle>
            Portfolio
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          link
          :to="`#${item.title.toLowerCase().replace(' ', '-')}`"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>


  <v-main>

    <slot/>

    <v-card width="100%" color="transparent">
            <v-spacer></v-spacer>
        <v-card-text>
          <div class="font-weight-bold ml-8 mb-2 text-center">
            Fotografie i grafiki użyte na stronie © Emilia Szafarowska 2021
          </div>
        </v-card-text>
      </v-card>

  </v-main>
  </v-app>
</template>

<script>
export default {
  metaInfo() {
    return {
      title: 'Portfolio'
    }
  },
  data(){
    return {
      items: [
        { title: 'O mnie', icon: 'mdi-account-box-outline' },
        { title: 'Fotografie', icon: 'mdi-camera-image' },
        { title: 'Projekty', icon: 'mdi-apps' },
      ]
    }
  }
}
</script>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
html {
  scroll-behavior: smooth;
}
.v-application--wrap {
  flex-direction: row !important;
  background-color: hsla(0,0%,100%,0.70) !important;
  background-image:url(IMG_20190902_195348.jpg) !important;
  background-blend-mode: overlay !important;
  background-size: cover !important;
}
.v-main {
  flex: 1 0 !important;
  margin-left: 240px !important;
}
</style>
