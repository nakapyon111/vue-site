<template>
  <section class="section section-works-list">
    <div class="container">
      <h1 class="page-ttl">WORKS</h1>
      <ListWork
        :works="
          works.slice(
            (Number($route.query[query] || 1) - 1) * limit,
            (Number($route.query[query] || 1) - 1) * limit + limit
          )
        "
      />
      <ItemPagination
        :total-page="parseInt((works.length + limit - 1) / limit)"
        :query="query"
        :now="Number($route.query[query] || 1)"
      />
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
  data() {
    return {
      query: 'page',
      limit: 6,
    }
  },
}
</script>

<style lang="scss" scoped>
.section-works-list {
  > .container {
    > .page-ttl {
      top: -62px;

      @include mq(sm) {
        top: -28px;
      }
    }

    > .list {
      margin-top: -16px;
    }

    > .item {
      margin-top: 32px;

      @include mq(md) {
        margin-top: 24px;
      }
    }
  }
}
</style>
