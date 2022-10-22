<template>
  <div class="section section-top-about-news">
    <div class="container">
      <section class="prof">
        <ContentProfSimple />
      </section>

      <section class="news">
        <div class="container">
          <h2 class="news-ttl">NEWS</h2>
          <ListNews :newses="newses" class="list-first" />
          <ButtonLink to="/news">ALL NEWS</ButtonLink>
        </div>
      </section>
    </div>
  </div>
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
.section-top-about-news {
  background: #fff;

  > .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 80px;

    @include mq(md) {
      display: block;
    }

    > .prof {
      width: 46%;
      max-width: 476px;
      padding: 0;

      @include mq(md) {
        width: 100%;
        margin: auto;
        padding-bottom: 40px;
      }
    }

    > .news {
      width: 50%;
      padding: 0 24px;
      background-color: var(--color-bg-gray);

      @include mq(md) {
        width: 100%;
        padding: 0;
        background-color: transparent;
      }

      > .container {
        max-width: 476px;
        padding-top: 48px;
        padding-bottom: 56px;

        @include mq(md) {
          max-width: none;
          padding-top: 40px;
          padding-bottom: 0;
        }

        > .news-ttl {
          font-size: 24px;
          line-height: 1.4em;
          letter-spacing: 0.08em;

          @include mq(md) {
            font-size: 32px;
          }

          @include mq(sm) {
            font-size: 23px;
          }
        }

        > .list {
          margin-top: 12px;

          @include mq(md) {
            margin-top: 28px;
          }

          @include mq(sm) {
            margin-top: 16px;
          }

          @include mq(xs) {
            margin-top: 12px;
          }

          @include mq(xxs) {
            margin-top: 0;
          }
        }

        > .button-link {
          max-width: 200px;
          margin: 12px auto 0;

          @include mq(md) {
            margin-top: 32px;
          }

          @include mq(xxs) {
            margin-top: 24px;
          }
        }
      }
    }
  }
}
</style>
