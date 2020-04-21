<template>
    <div>
        <home-header></home-header>
        <home-banner></home-banner>
        <home-icons></home-icons>
    </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeBanner from './components/Banner'
import HomeIcons from './components/Icons'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeBanner,
    HomeIcons
  }
}
</script>

<style lang='stylus' scoped>

</style>
