<template>
  <PageWrapper>
    <h1>Okay this is heading one</h1><h2>heading two</h2><h3>heading three</h3><p></p><p>this sentence will have something <strong>bold</strong> in it</p><p></p><p>this sentence will <em>emphasize </em></p><p></p><p><s>this sentence is redacted</s></p><p></p><p><u>this sentence is noted </u></p><p></p><p><code>this is highlighted</code></p><p></p><p></p>
  </PageWrapper>
</template>

<script>
import PageWrapper from '../components/PageWrapper'
export default {
  name: 'Home',
  components: { PageWrapper },
  data() {
    return {}
  }
}
</script>

<style lang="css" scoped>
</style>
