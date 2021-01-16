<template>
  <div class="searchWrapper">
      <input
        id="search"
        name="search"
        v-model="searchValue"
        @input="handleInput"
      />
  </div>
</template>
<script>

export default {
  name: 'SearchInput',
};
</script>
<style scoped>
.searchWrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
  width: 250px;
}
input {
  height: 30px;
  border: 0;
  border-bottom: 1px solid black;
  background: none;
}
</style>