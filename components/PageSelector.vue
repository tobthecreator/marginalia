<template>
  <div class="link-container">
    <nuxt-link
      class="link"
      to="/"
      :class="'/' === this.path ? 'link-active' : ''"
    >
      Home
    </nuxt-link>
    <nuxt-link
      class="link"
      :class="'/notes' === this.path ? 'link-active' : ''"
      to="/notes"
    >
      Notes
    </nuxt-link>
    <nuxt-link
      class="link"
      to="/about"
      :class="'/about' === this.path ? 'link-active' : ''"
    >
      About
    </nuxt-link>
    <nuxt-link
      class="link"
      to="/test"
      :class="'/test' === this.path ? 'link-active' : ''"
    >
      Test
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: 'PageSelector',
  data() {
    return {
      path: 'notes'
    }
  },
  methods: {
    isActive(selector) {
      return selector === this.path ? 'link-active' : ''
    }
  },
  beforeMount() {
    this.path = $nuxt.$route.path
    console.log(`PATH ${this.path}`)
  }
}
</script>

<style lang="css" scoped>
.link-container {
  margin: .75em;
  font-size: 1.2em;
  font-weight: bold;

}

.link {
  margin: 0.625em;
  color: rgba(118, 89, 255, 0.75)
}

.link:hover {
  color: rgba(97, 69, 226, 1);
}

.link-active {
  color: rgba(97, 69, 226, 1);
}
</style>
