<template>
  <div class="container">
      <img :src=b />
  </div>
</template>

<script>
import axios from "axios";

  export default {
    data() {
        return {
            b: []
        };
    },
    async created() {
        const config = {
            headers: {
                Accept: "application/json"
            }
        };

        try {
            const res =  await axios.get(`https://api.nasa.gov/planetary/apod?api_key=Nziub2olDbsrIt6ZyPtTNTdbI1HJgcLx9CvyEsIr`);
            this.b = res.data.hdurl;
        } catch (err) {
            console.log(err);
        }
      
    }
  }
</script>

<style scoped>
img{
    height: 900px;
    width: 1400px;
    object-fit: cover;
    padding-top: 1rem;
}
</style>