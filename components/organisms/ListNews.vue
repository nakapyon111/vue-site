<template>
  <ul class="list list-news-simple">
    <ListItemNews v-for="news in newses" :key="news.id" :news="news" />
  </ul>
</template>

<script>
export default {
  props: {
    newses: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.list-news-simple {
  transform: translateX(-20px);
  display: flex;
  flex-wrap: wrap;
  width: calc(100% + 40px);

  @include mq(md) {
    transform: translateX(-12px);
    width: calc(100% + 24px);
  }

  @include mq(sm) {
    transform: translateX(-8px);
    width: calc(100% + 16px);
  }

  @include mq(xs) {
    transform: none;
    width: 100%;
  }

  > .list-item {
    width: 50%;
    padding: 4px 20px;

    @include mq(md) {
      padding: 0 12px;
    }

    @include mq(sm) {
      padding: 0 8px;
    }

    @include mq(xs) {
      width: 100%;
      padding: 0;
      border-top: 1px solid var(--color-stroke-gray-light);
    }

    &:first-child {
      border-top: none !important;
    }
  }

  &.list-first {
    transform: none;
    width: 100%;

    > .list-item {
      width: 100%;
      padding: 0;
      border-top: 1px solid var(--color-stroke-gray-light);
    }
  }

  &.list-default-md {
    @include mq(md) {
      transform: translateX(-12px);
      width: calc(100% + 24px);
    }

    @include mq(sm) {
      transform: translateX(-8px);
      width: calc(100% + 16px);
    }

    @include mq(xs) {
      transform: none;
      width: 100%;
    }

    > .list-item {
      @include mq(md) {
        width: 50%;
        padding: 0 12px;
        border-top: none;
      }

      @include mq(sm) {
        padding: 0 8px;
      }

      @include mq(xs) {
        width: 100%;
        padding: 0;
        border-top: 1px solid var(--color-stroke-gray-light);
      }
    }
  }

  &.list-first > .list-item:first-child {
    border-top: none !important;
  }

  &.list-last-md > .list-item:last-child {
    // display: none;

    @include mq(md) {
      // display: block;
    }

    @include mq(xs) {
      // display: none;
    }
  }
}
</style>
