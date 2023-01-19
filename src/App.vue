<script>
import AppHeader from "./components/AppHeader.vue"
import AppMain from "./components/AppMain.vue"
import AppFooter from "./components/AppFooter.vue"

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<template>
  <div>
    <header>
      <AppHeader />
    </header>

    <main>
      <AppMain />
    </main>

    <footer>
      <AppFooter />
    </footer>
  </div>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
@use "./styles/partials/variables.scss" as *;
@use "bootstrap/scss/bootstrap.scss" as *;
body {
  font-family: 'Barlow Semi Condensed', sans-serif;
}

header{
  width: 100%;
  background-color: $CodGrayColor;
}

.wrapper-container{
  width: 75%;
  margin: 0 auto;

}

</style>
