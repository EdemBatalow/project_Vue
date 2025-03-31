<template>
  <v-container>
    <!-- Карусель объявлений -->
    <v-row justify="center">
      <v-col cols="12">
        <v-carousel>
          <v-carousel-item
            v-for="ad in ads"
            :key="ad.id"
            :src="ad.src"
            cover
          >
            <div class="ad-link">
              <v-btn color="error" :to="'/ad/' + ad.id">
                {{ ad.title }}
              </v-btn>
            </div>
          </v-carousel-item>
        </v-carousel>
      </v-col>
    </v-row>

    <!-- Grid объявлений -->
    <v-row>
      <v-col
        v-for="ad in ads"
        :key="ad.id"
        xs="12"
        sm="6"
        md="4"
      >
        <v-card>
          <v-img 
            :src="ad.src" 
            :lazy-src="ad.src"
            height="200px"
            contain
          ></v-img>
          <v-card-title>
            <h3 class="headline mb-1">{{ ad.title }}</h3>
            <p>{{ ad.desc }}</p>
          </v-card-title>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn text :to="'/ad/' + ad.id">Open</v-btn>
            <v-btn color="primary">Buy</v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      ads: [
        {
          title: "First",
          desc: "First Desc",
          src: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
          id: "1"
        },
        {
          title: "Second",
          desc: "Second Desc",
          src: "https://cdn.vuetifyjs.com/images/carousel/sky.jpg",
          id: "2"
        },
        {
          title: "Third",
          desc: "Third Desc",
          src: "https://cdn.vuetifyjs.com/images/carousel/bird.jpg",
          id: "3"
        },
        {
          title: "Fourth",
          desc: "Fourth Desc",
          src: "https://cdn.vuetifyjs.com/images/carousel/planet.jpg",
          id: "4"
        }
      ]
    };
  }
};
</script>

<style scoped>
.ad-link {
  position: absolute;
  bottom: 50px;
  left: 50%;
  background: rgba(0, 0, 0, 0.5);
  transform: translate(-50%, 0);
  padding: 5px 15px;
  border-radius: 5px;
}
</style>
