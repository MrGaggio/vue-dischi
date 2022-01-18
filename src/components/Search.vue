<template>
  <div>
    <label class="gendre mx-3" for="dischi">CHOOSE A GENDRE:</label>
    <select name="dischi" id="dischi"
    v-model="gendre"
    @change="$emit('doSearch', gendre)"
    >
      <input type="text" name="scegli" id="" />
      <option id="all" value="text">All</option>
      <option id="metal" value="text">Metal</option>
      <option id="pop" value="text">Pop</option>
      <option id="rock" value="text">Rock</option>
      <option id="jazz" value="text">Jazz</option>
    </select>
  </div>
</template>

<script>
export default {
    name: 'Search',
    data (){
        return {
            gendre: ""
        }
    }
};
</script>

<style></style>
