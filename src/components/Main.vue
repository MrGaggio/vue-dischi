<template>
  <main>
    <div class="container">
      <div class="row cards">
        <div class="col-2 card mx-3 my-2">
            <img
            src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg"
            alt="Prova"
             />
            <h2 class="f2-bold" >New Jersey</h2>
            <h5 class="fs-5 my-0">Bon Jovi</h5>
            <h6 class="fs-6">1980</h6>
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
main {
  background-color: #1e2d3b;
  height: 1000px;
  text-align: center;
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
  padding-bottom: 50px;
}
</style>
