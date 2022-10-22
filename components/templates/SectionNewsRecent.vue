<template>
  <section class="section section-news-recent">
    <div class="container">
      <h2 class="section-ttl-small">RECENT NEWS</h2>
      <ListNews :newses="newsesRecent" />
      <ButtonLink to="/news">ALL NEWS</ButtonLink>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    newsesRecent: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.section-news-recent {
  > .container {
    padding-top: 40px;

    > .list {
      margin-top: 16px;
    }

    > .button-link {
      max-width: 200px;
      margin: 24px auto 0;
    }
  }
}
</style>
