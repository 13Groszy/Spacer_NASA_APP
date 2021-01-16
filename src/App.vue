<template>
  <div class="wrapper">
    <HeroImage />
    <Claim />
    <SearchInput :value="searchValue" v-model="searchValue" @input="handleInput"/>
  </div>
</template>

<script>
import axios from "axios";
import debounce from "lodash.debounce";
import Claim from "@/components/Claim";
import SearchInput from "@/components/SearchInput";
import HeroImage from "@/components/HeroImage";

const API = "https://images-api.nasa.gov/search";

export default {
  name: "App",
  components: {
    Claim,
    SearchInput,
    HeroImage,
  },
  data() {
    return {
      searchValue: "",
      results: [],
    };
  },
  methods: {
    handleInput: debounce(function () {
      console.log(this.searchValue)
      axios
        .get(`${API}?q=${this.searchValue}&media_type=image`)
        .then((response) => {
          this.results = response.data.collection.items;
        })
        .catch((error) => {
          console.log(error);
        });
    }, 500),
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;500;600&display=swap");
* {
  box-sizing: border-box;
}
body {
  font-family: "Oswald", sans-serif;
  margin: 0;
  padding: 0;
}
.wrapper {
  margin: 0;
  width: 100%;
  min-height: 100vh;
  padding: 30px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
