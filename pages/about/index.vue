<template>
  <article class="page page-about">
    <SectionAboutProfile />
    <SectionAboutCareer />
  </article>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.page-about {
  @include mq(sm) {
    padding-bottom: 80px;
  }
}
</style>
