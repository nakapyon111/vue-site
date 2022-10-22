<template>
  <!-- eslint-disable-next-line vue/no-v-html -->
  <div class="content content-article" v-html="article" />
</template>

<script>
export default {
  props: {
    article: {
      type: String,
      required: true,
    },
  },
}
</script>

<style lang="scss">
.content-article {
  max-width: 960px;
  padding-right: 40px;

  @include mq(sm) {
    padding-right: 0;
  }

  > * {
    margin-top: 40px;

    @include mq(sm) {
      margin-top: 24px;
    }
  }

  figure {
    display: flex;
    max-width: 100%;

    > .wp-block-embed__wrapper {
      position: relative;
      display: flex;
      width: 100%;

      &::before {
        content: '';
        width: 100%;
        padding-top: 56.25%;
      }

      > iframe {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        width: 100%;
        height: 100%;
      }
    }
  }

  h2 {
    margin-top: 64px;
    font-size: 24px;

    & + * {
      margin-top: 24px;
    }
  }

  *:first-child {
    margin-top: 0 !important;
  }

  a {
    text-decoration: underline;
    transition: all 0.024s linear;

    &:hover {
      color: var(--color-font-black-64);
    }
  }
}
</style>
