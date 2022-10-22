<template>
  <section class="section section-top-works">
    <div class="container">
      <h2 class="works-ttl">WORKS</h2>
      <ListWork :works="works" />
      <ButtonLink to="/works">ALL WORKS</ButtonLink>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    works: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.section-top-works {
  > .container {
    margin-top: 80px;
    margin-bottom: 120px;

    @include mq(md) {
      margin-top: 40px;
      margin-bottom: 80px;
    }

    > .list {
      margin-top: 24px;

      @include mq(sm) {
        margin-top: 12px;
      }

      @include mq(xxs) {
        margin-top: 0;
      }
    }

    > .button {
      max-width: 400px;
      margin: 32px auto 0;
      padding: 16px;

      @include mq(md) {
        max-width: 200px;
        padding: 12px;
      }

      @include mq(sm) {
        margin-top: 24px;
      }
    }
  }
}
</style>
