<template>
  <section class="section section-about-career">
    <div class="container js-scroll">
      <h2 class="career-ttl">CAREER</h2>
      <div class="career-history">
        <div class="career-history-items">
          <p v-for="(h, i) in history" :key="i" class="career-history-item">
            {{ h.time }}&nbsp;&nbsp;{{ h.text }}
          </p>
        </div>
        <figure class="career-history-fig career-history-fig-1">
          <picture class="career-history-fig-img js-scroll">
            <img
              src="/imgs/page/about/amitysensei-about-career-1.jpg"
              alt="amity_senseiの画像1"
              loading="lazy"
            />
          </picture>
        </figure>
        <figure class="career-history-fig career-history-fig-2">
          <picture class="career-history-fig-img js-scroll">
            <img
              src="/imgs/page/about/amitysensei-about-career-2.jpg"
              alt="amity_senseiの画像2"
              loading="lazy"
            />
          </picture>
        </figure>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      history: [
        {
          time: '2012',
          text: '京都市立銅駝学校美術工芸高等学校 卒業',
        },
        {
          time: '2016',
          text: 'University for the Creative Arts 卒業',
        },
        {
          time: '2016',
          text: '株式会社 Momentum Japan 入社',
        },
        {
          time: '2018',
          text: '株式会社 TBWA HAKUHODO 入社',
        },
        {
          time: '2019',
          text: '独立 / 株式会社olio設立',
        },
        {
          time: '2019',
          text: 'iPadに特化したオンラインサロン「iPadmate」開設',
        },
        {
          time: '2020',
          text: 'Adobe MAX 2020 登壇',
        },
        {
          time: '2020',
          text: '著書「iPadクリエイティブ」発売',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.section-about-career {
  > .container {
    padding-top: 40px;

    > .career-history {
      position: relative;
      display: flex;
      justify-content: space-between;
      align-items: flex-end;
      margin-top: 24px;
      padding-top: 168px;

      @include mq(sm) {
        flex-wrap: wrap;
        justify-content: center;
        padding-top: 0;
      }

      > .career-history-items {
        position: absolute;
        top: 0;
        left: 0;
        z-index: 1;

        @include mq(sm) {
          position: initial;
          width: 100%;
        }
      }

      > .career-history-fig {
        position: relative;
        display: flex;
        width: 50%;

        &::before {
          content: '';
          width: 100%;
        }

        > .career-history-fig-img {
          position: absolute;
          top: 0;
          right: 0;
          bottom: 0;
          left: 0;

          &.js-scroll {
            // opacity: 0;
            transform: translate3d(0, 24px, 0);
            transition: all 2.8s cubic-bezier(0, 0.55, 0.45, 1);

            &.js-scroll-active {
              // opacity: 1;
              transform: translate3d(0, 0, 0);
            }
          }
        }

        &.career-history-fig-1 {
          transform: translateX(-6%);

          @include mq(sm) {
            margin-top: 40px;
          }

          @include mq(xs) {
            transform: translateX(-56px);
            min-width: 264px;
            min-height: 360px;
          }

          &::before {
            padding-top: 154.8148148148148%;
          }
        }

        &.career-history-fig-2 {
          margin-bottom: 40px;
          z-index: -1;

          @include mq(xs) {
            margin-top: -40px;
            margin-bottom: 0;
            transform: translateX(40px);
            min-width: 240px;
            min-height: 320px;
          }

          &::before {
            padding-top: 120%;
          }
        }
      }
    }
    &.js-scroll {
      // opacity: 0;
      transform: translate3d(0, 24px, 0);
      transition: all 2.8s cubic-bezier(0, 0.55, 0.45, 1);

      &.js-scroll-active {
        // opacity: 1;
        transform: translate3d(0, 0, 0);
      }
    }
  }
}
</style>
