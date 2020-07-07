<template>
  <div>
    <Navigation />
    <Nuxt />
  </div>
</template>

<script>
import axios from "axios"

export default {
  data() {
    return {
      
    }
  },
  created() {

  },
  asyncData ({ params, error }) {
    return axios.get(`http://dg-sport.local/wp-json/wuxt/v1/menu`).then((res) => {
        console.log(res.data);
        return { navigation: res.data }
    }).catch((e) => {
        error({ statusCode: 404, message: 'Menu non trouvé' })
    })
  }
}
</script>

<style>

</style>
