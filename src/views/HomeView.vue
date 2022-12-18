<template>

  <Header />

  <Member />

</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Member from '@/components/Member.vue'

export default {
  name: 'HomeView',
  components: {
    Header,
    Member
  }
}
</script>

<style scoped lang="scss">
img {
  width: 200px;
}
</style>
