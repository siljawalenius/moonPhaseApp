<template>
  <div class="search-box">
    <input 
        type="text" 
        class="search-bar" 
        placeholder="Search..." 
        v-model="city"
        />
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  
};
</script>

<style scoped></style>
