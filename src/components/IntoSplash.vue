<template>
  <div class="banner-wrap">
    <img alt="chicken" class="logo" src="@/assets/chicken.svg" />
    <div class="banner">
      <h2><span>Buddy</span></h2>
      <h1>Coward</h1>
      <h5><span>Face your Constituency</span></h5>
    </div>
  </div>
</template>

<script setup lang="ts">
</script>

<style>
.logo {
  width: 50%;
}
.banner-wrap {
  display: flex;
  position: relative;
}

.banner {
  font-size: 2.3rem;
  line-height: 0.8;
  text-align: right;
  position: absolute;
  margin-top: 100px;
}

@media (min-width: 1024px) {
  .banner h5, h1, h2 {
    text-shadow: 4px 4px 5px black;
  }
  .banner h5 {
    line-height: 2.5;
  }
  .banner h1, h2 {
    font-size: 10vw;
    line-height: 0.6;
  }
  .logo {
    right: 150px;
  }
}

</style>
