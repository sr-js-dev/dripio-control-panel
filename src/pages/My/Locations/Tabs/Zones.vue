<template>
  <div class="flex absolute-center">
    <q-img
      style="height: 200px; width: 200px"
      :ratio="19/11"
      src="/statics/placeholders/under-construction.png"
    >
      <div class="absolute-top">
        <div class="text-h4">Zones</div>
      </div>
    </q-img>
  </div>
</template>

<style>
</style>

<script>
import { mapGetters } from 'vuex'

export default {
  name: 'LocationDetails',
  props: ['locationId'],
  data: () => ({}),

  computed: {
    ...mapGetters({
      me: 'auth/currentUser'
    }),
    location() {
      return this.$store.getters['locations/byId'](this.locationId)
    }
  }
}
</script>
