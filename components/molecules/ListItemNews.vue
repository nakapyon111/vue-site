<template>
  <li class="list-item list-item-news">
    <nuxt-link :to="`/news/${news.slug}`" class="news-link">
      <figure class="news-fig">
        <picture class="news-fig-img">
          <img
            :src="news.source_url"
            :alt="news.title.rendered"
            loading="lazy"
          />
        </picture>
      </figure>
      <div class="news-info">
        <h3 class="news-ttl font-500">
          {{ news.title.rendered }}
        </h3>
        <time class="new-time">
          {{ $dayjs(news.date).format('YYYY.MM.DD') }}
        </time>
      </div>
    </nuxt-link>
  </li>
</template>

<script>
export default {
  props: {
    news: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.list-item-news {
  > .news-link {
    padding: 12px 0;

    @include mq(sm) {
      padding: 8px 0;
    }

    @include mq(xs) {
      padding: 12px 0;
    }

    > .news-fig {
      flex: 1;
      position: relative;
      display: flex;
      min-width: 40%;
      min-height: 104px;
      overflow: hidden;

      @include mq(sm) {
        min-height: 80px;
      }

      &::before {
        content: '';
        width: 100%;
        padding-top: 60%;
      }

      > .news-fig-img {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        transform: scale(1);
        transition: all 0.16s cubic-bezier(0.11, 0, 0.5, 0);
      }
    }

    > .news-info {
      width: 280px;
      min-width: 60%;
      padding-top: 12px;
      padding-left: 16px;

      @include mq(sm) {
        padding-top: 8px;
      }

      > .news-ttl,
      > .news-time {
        line-height: 1.4em;
      }

      > .news-ttl {
        font-size: 16px;

        @include mq(sm) {
          font-size: 14px;
        }
      }

      > .news-time {
        display: inline-block;
        width: 100%;
        margin-top: 8px;
        font-size: 12px;
        color: var(--color-font-gray);

        @include mq(sm) {
          margin-top: 4px;
        }
      }
    }

    &:hover {
      > .news-fig {
        > .news-fig-img {
          transform: scale(1.12);
        }
      }
    }
  }
}
</style>
