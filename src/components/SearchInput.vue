<template>
  <input id="search"
  name="search"
  :class="{dark}"
  :value="value"
  @input="handleChange" />
</template>
<script>
export default {
  name: "SearchInput",
  props: {
    value: {
      type: String,
      required: true,
    },
  dark: {
    type: Boolean,
    default: false,
    },
  },
  methods: {
    handleChange(e) {
      this.$emit("input", e.target.value);
    },
  },
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;500;600&display=swap");
body {
  font-family: "Oswald", sans-serif;
}
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
.dark{
color:rgb(15, 206, 142);
border-bottom-color:rgb(15, 206, 142);
}
.dark:focus{
box-shadow: 0 10px 15px -8px rgba(15, 206, 142, .5);
}
</style>