<template>
  <div class="home">
    <div class="home_inner">
    
      
    </div>
  </div>
</template>

<script>

</script>

<style lang="scss">
@import "~@/assets/scss/variables";
@import "~@/assets/scss/mixins";

.home {
  min-height:      100vh;
  background:      $primary;
  display:         flex;
  align-items:     center;
  justify-content: center;

  &__inner {
    display:        flex;
    flex-direction: column;
  }
}
</style>
