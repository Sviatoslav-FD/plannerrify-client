<template>
  <div class="home">
    <HomeHeader />
    <HomeHero />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import { HomeHeader, HomeHero, Button } from '@/components/shared'

@Options({
	name: 'Home',
	components: { HomeHeader, HomeHero, Button }
})
export default class Home extends Vue {}
</script>

<style lang="scss" scoped>
.home {
  height: 100%;
  display: flex;
  flex-direction: column;
}
</style>
