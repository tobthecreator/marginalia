<template>
  <PageWrapper>
    <form
      class="form_container"
      action="https://tinyletter.com/tobthecreator"
      method="post"
      target="popupwindow"
      onsubmit="window.open('https://tinyletter.com/tobthecreator', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true">
        <b>Enter your email address</b>
        <p>
          <input class="email_input" type="text" style="width:200px" name="email" id="tlemail" />
        </p>
        <input type="hidden" value="1" name="embed" />
        <input class="subscription_button" type="submit" value="Subscribe" />
        <p>
          <a href="https://tinyletter.com" target="_blank">
            powered by TinyLetter
          </a>
        </p>
    </form>
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

<style lang="css">
.form_container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}


.email_input {
  height: 2em;
  font-size: 1em;
  border-radius: 0.5em;
  text-indent: 0.25em;
  border: 2px solid #222;
  padding: 0.5em;
  margin-top: 0.5em;
}

.email_input:focus,
.email_input:hover {
  outline: none;
  border: 2px solid rgba(118, 89, 255, 0.75);
}

.subscription_button {
  width: 100px;
  height: 35px;
  font-size: 1em;
  border: 2px solid #222;
  border-radius: 0.5em;
  margin: 0.5em;
  cursor: pointer;
  font-weight: bold;
}

.subscription_button:focus,
.subscription_button:hover {
  outline: none;
  border: 2px solid rgba(118, 89, 255, 0.75);
  color: rgba(118, 89, 255, 0.75);
}

.subscription_button:active, {
  transform: scale(.975);
}
</style>
