<template>
  <div>
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <nuxt-link :to="localePath('/')" class="navbar-brand">BoilerPlate</nuxt-link>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav">
                <li  class="nav-item">
                    <nuxt-link :to="localePath('/realisations/')" class="nav-link">Réalisations</nuxt-link>
                </li>
                <li  class="nav-item">
                    <nuxt-link :to="localePath('/services/')" class="nav-link">Services</nuxt-link>
                </li>
            </ul>
            <ul class="navbar-nav ml-auto">
              <li class="nav-item ">
                <nuxt-link class="nav-link"
                  v-if="$i18n.locale !== 'fr'"
                  :to="switchLocalePath('fr')"
                >
                  fr
                </nuxt-link>

                <nuxt-link class="nav-link"
                  v-if="$i18n.locale !== 'de'"
                  :to="switchLocalePath('de')"
                >
                  de
                </nuxt-link>
              </li>
            </ul>
        </div>
        </nav>
  </div>
</template>

<script>

export default {
  data() {
    return {
      
    }
  }
}
</script>

<style>

</style>