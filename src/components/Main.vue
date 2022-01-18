<template>
  <main>
    <div class="container">
      <div class="row cards">
        <div class="col-2 card mx-3 my-2"
        :key="index" 
        v-for="(cover, index) in covers"
        >
            <img
            :src="cover.poster"
            alt=""
             />
            <h2 class="f2-bold">
                {{ cover.title }}
            </h2>
            <h5 class="fs-5 my-0">
                {{ cover.author }}
            </h5>
            <h6 class="fs-6">
                {{ cover.year }}
            </h6>
        </div>
        
      </div>
    </div>
  </main>
</template>

<script>
import axios from 'axios';
export default {
  name: "Main",

  data() {
    return {
      covers: null,
    };
  },
    mounted (){
    axios.get ('https://flynn.boolean.careers/exercises/api/array/music')
    .then((result) => {
        // console.log(result);
        this.covers = result.data.response
        console.log(this.covers);
    })
    .catch((error) => {
        console.log(error);
    })
  },
};
</script>

<style lang="scss">
body{
    background-color: #1e2d3b;
}

main {
  text-align: center;
  overflow-y: hidden;
  background-color: #1e2d3b;
}
h2{
    color: white;
    padding-top: 10px;
}
h5, h6 {
    color: #75756F;
}

.container {
  padding-top: 50px;
}
.card {
  background-color: #2e3a46 !important;
  padding-top: 20px;
  
}
</style>
