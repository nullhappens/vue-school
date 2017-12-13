<template>
  <div class="col-full" :style="$style.centered">
    <h1 :class="$style.headingLarge">Not Found</h1>
    <p :class="$style.textLarge">
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

<style module>
  .headingLarge{
    font-size: 100px;
  }
  .textLarge {
    font-size: 50px;
    font-weight: 100;
  }
  .centered {
    text-align: center;
  }
</style>
