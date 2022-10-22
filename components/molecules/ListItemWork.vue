<template>
  <li class="list-item list-item-work">
    <nuxt-link :to="`/works/${work.slug}`" class="work-link">
      <figure class="work-fig">
        <picture class="work-fig-img">
          <img src="/imgs/page/top/work-thumb.jpg" alt="" />
        </picture>
      </figure>
      <div class="work-info">
        <div class="work-info-cont">
          <time class="work-time">
            {{ $dayjs(work.date).format('YYYY.MM.DD') }}
          </time>
          <h3 class="work-ttl font-500">
            {{ work.title.rendered }}
          </h3>
          <p class="work-client">
            {{ work.acf.client }}
          </p>
        </div>
      </div>
    </nuxt-link>
  </li>
</template>

<script>
export default {
  props: {
    work: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.list-item-work {
  > .work-link {
    position: relative;

    @include mq(md) {
      display: block;
    }

    > .work-fig {
      position: relative;
      display: flex;
      width: 100%;
      max-height: 447px;
      overflow: hidden;

      &::before {
        content: '';
        width: 100%;
        padding-top: 130%;
      }

      > .work-fig-img {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        transform: scale(1);
        transition: all 0.16s cubic-bezier(0.11, 0, 0.5, 0);
      }
    }

    > .work-info {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      padding: 20px;
      background-color: transparent;
      transition: all 0.024s linear;

      @include mq(md) {
        position: initial;
        padding: 8px 0 0;
        background-color: transparent;
      }

      @include mq(sm) {
        padding-top: 0;
      }

      > .work-info-cont {
        height: 100%;
        padding-top: 80%;
        opacity: 0;
        transition: all 0.024s linear;

        @include mq(md) {
          padding-top: 0;
          opacity: 1;
        }

        > .work-time,
        > .work-ttl,
        > .work-client {
          line-height: 1.4em;
          color: var(--color-font-white);

          @include mq(md) {
            color: var(--color-font-default);
          }
        }

        > .work-time {
          display: inline-block;
          width: 100%;

          @include mq(sm) {
            font-size: 10px;
          }
        }

        > .work-ttl {
          //margin-top: 4px;
          font-size: 20px;

          @include mq(md) {
            font-size: 16px;
          }

          @include mq(sm) {
            font-size: 14px;
          }
        }

        > .work-hr {
          //width: 24%;
          width: 0;
          max-width: 64px;
          margin-top: 6px;
          margin-bottom: 0;
          border-color: var(--color-stroke-gray);
          transition: all 0.24s cubic-bezier(0.11, 0, 0.5, 0);

          @include mq(md) {
            width: 24%;
            min-width: 32px;
          }
        }

        > .work-client {
          margin-top: 4px;

          @include mq(sm) {
            font-size: 10px;
          }
        }
      }
    }

    &:hover {
      > .work-fig {
        > .work-fig-img {
          @include mq(md) {
            transform: scale(1.04);
          }
        }
      }

      > .work-info {
        background-color: var(--color-bg-black-88);

        @include mq(md) {
          background-color: transparent;
        }

        > .work-info-cont {
          opacity: 1;

          > .work-hr {
            width: 24%;
          }
        }
      }
    }
  }
}
</style>
