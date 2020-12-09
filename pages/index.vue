<template>
  <div>
    <section class="section">
      <h1 class="title">Ryan Augustynowicz</h1>
      <h2 class="subtitle">Software Developer at the <a href="http://cdp.uwo.ca/">Centre for Digital Philosophy</a></h2>
      <p>Interests: <b>Software development, Veganism, Animals,</b> Fitness, Travel, Philosophy, Sociology</p> 
      <br />
      <span v-for="image in images" v-bind:key="image.pathLong"> 
        <img :src="image.pathLong" class="featured-image">
        <br />
      </span>
    </section>
  </div>
</template>

<script>

export default {
  // Get all images from dir - https://stackoverflow.com/q/54095215
  name: 'HomePage',
  components: {
  },
  head() {
    return {
      title: 'Ryan Augustynowicz - Software Developer in London Ontario'
    }
  },
  data() {
    return {
      images: [],
    };
  },

  mounted() {
    this.importAll(require.context('../assets/featured_images/', true, /\.jpg$/));
  },

  methods: {
    importAll(r) {
      r.keys().forEach(key => (this.images.push({ pathLong: r(key), pathShort: key })));
    },
  },
}
</script>
<style lang="scss">
.featured-image {
  max-height: 70vh;
}
</style>