<template>
  <div class="container">
    <div class="columns is-mobile is-marginless is-centered">
      <div class="column is-narrow title is-paddingless">marginalia</div>
    </div>
    <div class="columns is-mobile is-marginless is-centered">
      <div class="column is-narrow is-paddingless">
        <PageSelector />
      </div>
    </div>

    <div class="columns is-mobile is-marginless is-centered">
      <div class="column content is-half-desktop is-four-fifths-mobile is-paddingless">
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

.title {
  font-size: 3em;
  font-weight: bold;
}

</style>
