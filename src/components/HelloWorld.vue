<template>
  <v-container>
    <div class="container-cols">
      <div v-for="(image, index) in images" :key="index" md="auto" class="img-container">
        <v-lazy
          :options="{
            threshold: .5
          }"
          class="lazy-container"
          transition="fade-transition">
          <v-dialog
            width="500"
          >

            <template>
              <v-carousel v-model="model" hide-delimiters>
                <v-carousel-item
                  v-for="(img, i) in images"
                  :key="i"
                >

                  <v-sheet
                    color="#ffffff"
                    height="100%"
                    tile
                  >
                    <v-row
                      class="fill-height"
                      align="center"
                      justify="center"
                    >
                    
                      <v-img
                        outlined 
                        tile 
                        :src="img"></v-img>

                    </v-row>

                  </v-sheet>

                </v-carousel-item>
              </v-carousel>
            </template>

            <template v-slot:activator="{ on, attrs }">
        
              <v-img 
                class="feed-imgs"
                outlined 
                tile 
                v-on:click="model = index"
                :src="image" 
                v-bind="attrs"
                v-on="on"></v-img>

            </template>
          </v-dialog>
        </v-lazy>
      </div>
    </div>

  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',

    data: () => {
      return {
        model: 0,
        images: [
          require("../assets/photos/v10.jpg"),
          require("../assets/photos/v1.jpeg"),
          require("../assets/photos/v7.jpg"),
          require("../assets/photos/v2.jpeg"),
          require("../assets/photos/v3.jpeg"),
          require("../assets/photos/v4.jpeg"),
          require("../assets/photos/v9.jpg"),
          require("../assets/photos/v5.jpeg"),
          require("../assets/photos/v8.jpg"),
          require("../assets/photos/v11.jpeg"),
          require("../assets/photos/v12.jpeg"),
          require("../assets/photos/v13.jpeg"),
          require("../assets/photos/v14.jpeg"),
          require("../assets/photos/v15.jpeg"),
          require("../assets/photos/v16.jpeg"),
          require("../assets/photos/v17.jpeg"),
          require("../assets/photos/v18.jpeg"),
          require("../assets/photos/v19.jpeg"),
          require("../assets/photos/v20.jpeg"),
          require("../assets/photos/v21.jpeg"),
          require("../assets/photos/v22.jpeg"),
          require("../assets/photos/v23.jpeg"),
          require("../assets/photos/v24.jpeg"),
          require("../assets/photos/v25.jpeg"),
          require("../assets/photos/v26.jpeg"),
          require("../assets/photos/v27.jpeg"),
          require("../assets/photos/v28.jpeg"),
          require("../assets/photos/v29.jpeg"),
          require("../assets/photos/v30.jpeg"),
          require("../assets/photos/v31.jpeg"),
          require("../assets/photos/v32.jpeg"),
          require("../assets/photos/v33.jpeg"),
          require("../assets/photos/v34.jpeg"),
          require("../assets/photos/v35.jpeg"),
          require("../assets/photos/v36.jpeg"),
          ],
      };
    }
  }
</script>

<style>

  .container-cols {
    display: flex;
    flex-wrap: wrap;
    margin: 5px;
  }

  v-carousel-item > img {
    margin: auto;
  }

  .img-container {
    margin: 5px auto 5px auto !important;
    width: 30%;
    display: flex;
  }

  .img-container > div {
    margin: auto;
  }

  .feed-imgs {
    width: 21.3rem;
    border-radius: 2.5px;
  }

  v-sheet {
    background: white;
    display: flex;
    margin: auto;
  }

  @media only screen and (min-width: 769px) {
    .feed-imgs:hover {
      animation-name: grow;
      animation-duration: 300ms;
      width: 23rem;
    }
  
  }

  @media only screen and (max-width: 768px) {
    .feed-imgs {
      width: 7.5rem;
    }
  }

  @keyframes grow {
    from {
      box-shadow: initial;
      width: 21.3rem;
    }

    to {
      width: 23rem;
    }

  }

</style>