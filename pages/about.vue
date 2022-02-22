<template>
  <default-view title="About Page Title">
    <div class="md:flex md:gap-10">
      <img :src="team" class="w-full md:w-1/3 rounded" />
      <div>
        <h2 class="font-bold text-2xl">About our <span class="font-team">team</span></h2>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Incidunt eos
          rem commodi architecto necessitatibus magnam consectetur alias sit
          esse nostrum ab natus nobis, excepturi a, ullam consequatur. Veritatis
          ipsum quibusdam rem aliquid reiciendis ea aliquam, sunt sed a optio
          maxime.onsequatur. Veritatis ipsum quibusdam rem aliquid reiciendis ea
          aliquam, sunt sed a optio maxime.
        </p>
      </div>
    </div>
  </default-view>
</template>

<script>
import DefaultView from '../layouts/DefaultView.vue'
import imgTeam from '../static/images/team.jpg'
export default {
  name: 'AboutPage',
  components: { DefaultView },
  data() {
    return {
      team: imgTeam,
    }
  },
}
</script>

<style lang="css" scoped>
  .font-team {
    color: green
  }
</style>>

</style>