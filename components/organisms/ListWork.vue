<template>
  <ul class="list list-work">
    <ListItemWork v-for="work in works" :key="work.id" :work="work" />
  </ul>
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
.list-work {
  transform: translateX(-12px);
  display: flex;
  flex-wrap: wrap;
  width: calc(100% + 24px);

  @include mq(md) {
    transform: translateX(-8px);
    width: calc(100% + 16px);
  }

  > .list-item {
    width: calc(100% / 3);
    padding: 16px 12px;

    @include mq(md) {
      padding: 16px 8px;
    }

    @include mq(xs) {
      width: 50%;
    }
  }
}
</style>
