<template>
  <section class="section section-news-list">
    <div class="container">
      <h1 class="page-ttl">NEWS</h1>
      <ListNews
        :newses="
          newses.slice(
            (Number($route.query[query] || 1) - 1) * limit,
            (Number($route.query[query] || 1) - 1) * limit + limit
          )
        "
      />
      <ItemPagination
        :total-page="parseInt((newses.length + limit - 1) / limit)"
        :query="query"
        :now="Number($route.query[query] || 1)"
      />
    </div>
  </section>
</template>

<script>
export default {
  props: {
    newses: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      query: 'page',
      limit: 12,
    }
  },
}
</script>

<style lang="scss" scoped>
.section-news-list {
  > .container {
    > .page-ttl {
      top: -62px;

      @include mq(md) {
        top: -66px;
      }

      @include mq(sm) {
        top: -36px;
      }

      @include mq(xs) {
        top: -32px;
      }
    }

    > .list {
      margin-top: -16px;

      @include mq(md) {
        margin-top: -12px;
      }

      @include mq(sm) {
        margin-top: -8px;
      }

      @include mq(xs) {
        margin-top: -12px;
      }
    }

    > .item {
      margin-top: 28px;

      @include mq(md) {
        margin-top: 32px;
      }
    }
  }
}
</style>
