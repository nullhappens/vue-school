<template>
  <div class="col-full">
    <h1>Not Found</h1>
    <p class="text-large">
      Oops, we couldn't find what you are looking for.  Try going 
      <router-link :to="{name: 'PageHome'}">
        home
      </router-link>
      instead?
    </p>
  </div>
</template>

<script>
</script>

<style scoped>
  h1 {
    font-size: 100px;
  }
  .text-large {
    font-size: 50px;
    font-weight: 100;
  }
  div {
    text-align: center;
  }
</style>
