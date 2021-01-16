<template>
  <input id="search"
  name="search"
  :value="value"
  @input="handleChange" />
</template>
<script>
export default {
  name: 'SearchInput',
  props: {
    value: {
    type: String,
    required: true,
    },
  },
methods: {
  handleChange(e){
this.$emit('input', e.target.value);
  }
}
};
</script>
<style scoped>
input {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 50px;
  width: 250px;
  height: 30px;
  border: 0;
  border-bottom: 1px solid black;
  background: none;
}
input:focus {
  outline: none;
  box-shadow: 0 10px 15px -8px rgb(0, 0, 0);
}
</style>