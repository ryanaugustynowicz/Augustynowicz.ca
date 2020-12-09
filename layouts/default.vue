<template>
  <div>
    <div class="cover"></div>
    <section class="main-content pop-out-desktop">
      <div class="container has-text-centered">
        <nuxt />
      </div>
    </section>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>
<style lang="scss">
.cover {
  background-color: #A5C6BB;
  height: 5vh;
  width: 100%;
}
.pop-out-desktop {
  background-color: #ffffff;
  width: 90%;
  position: relative;
  top: 3%;
  left: 5%;
  height: auto;
  overflow: visible;
}
</style>
