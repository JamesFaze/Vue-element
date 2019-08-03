<template lang="html">
    <div>
        <re-topnav></re-topnav>
        <re-nav></re-nav>
        <re-count></re-count>
    </div>
</template>

<script>
import ReTopnav from './components/ReTopNav'
import ReNav from './components/ReNav'
import ReCount from './components/ReCount'
export default {
    name:'Home',
    components: {
        ReTopnav,
        ReNav,
        ReCount,
    }
}
</script>

<style scoped>

</style>
