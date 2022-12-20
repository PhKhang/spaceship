<template>

  <Header />

  <Member />

  <Break />

  <Project />

  <Break />

  <Gallery />

  <Break />

  <Video />

  <Break />

</template>

<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Member from '@/components/Member.vue'
import Project from '@/components/Project.vue'
import Break from '@/components/Break.vue'
import Video from '@/components/Video.vue'
import Gallery from '@/components/Gallery.vue'

export default {
  name: 'HomeView',
  components: {
    Header,
    Member,
    Project,
    Break,
    Video,
    Gallery
  }
}
</script>

<style scoped lang="scss">
img {
  width: 200px;
}
</style>
