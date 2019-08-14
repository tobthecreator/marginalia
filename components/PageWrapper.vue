<template>
  <div class="container">
    <div class="columns is-mobile is-marginless is-centered">
      <div class="column is-narrow h1 is-paddingless"><b>marginalia</b></div>
    </div>
    <div class="columns is-mobile is-marginless is-centered">
      <div class="column is-narrow is-paddingless">
        <PageSelector />
      </div>
    </div>

    <div class="columns content is-mobile is-marginless is-centered">
      <div class="column is-half-desktop is-four-fifths-mobile is-paddingless">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
import PageSelector from '../components/PageSelector'
export default {
  name: 'DefaultTemplate',
  components: { PageSelector },
  data() {
    return {}
  }
}
</script>

<style lang="css">
.container {
  margin-top: 50px;
  margin-bottom: 50px;
}

.content {
  margin-top: 2em;
  margin-left: 10px;
  margin-right: 10px;
}

.h1 {
  font-size: 3em;
}
</style>
