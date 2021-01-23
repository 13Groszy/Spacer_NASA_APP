<template>
  <div class="claimWrapper">
    <h1 class="claim">SPACER</h1>
    <p class="subclaim">
      Lucas ipsum dolor sit amet plo wroonian meridian monkey-lizard ooryl
      barabel kiffar vulptereen jobal sykes.
    </p>
    <p class="subclaim">
      Vau aleena anthos ralter oola sith kessel. Gwurran vodran chewbacca moore
      greeata luminara.
    </p>
  </div>
</template>
<script>
export default {
  name: "Claim",
};
</script>
<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Oswald:wght@200;500;600&display=swap");
body {
  font-family: "Oswald", sans-serif;
}
.claimWrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.claim {
  font-size: 60px;
  margin: 0;
}
.subclaim {
  margin: 20px 0 0 0;
  font-size: 15px;
}
</style>