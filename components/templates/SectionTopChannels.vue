<template>
  <section class="section section-top-channels">
    <div class="container js-scroll">
      <figure class="ch-fig js-scroll">
        <picture class="ch-fig-img">
          <img
            src="/imgs/page/top/amitysensei-top-ch.jpg"
            alt="amity_senseiのYouTubeチャンネル"
            loading="lazy"
          />
        </picture>
      </figure>
      <div class="ch-txts">
        <h2 class="ch-ttl">CHANNELS</h2>
        <p class="ch-txt">
          現在、3つのYouTubeチャンネルを運営しています。主にiPadのクリエイティブな使い方を発信しているメインのチャンネルは、2019年12月に開設後、半年ほどで登録者10万人を超えました。そして現在は、ありがたいことに登録者25万人目前です。
          その他に、メインチャンネルの英語版とiPhoneの使い方やガジェット紹介のサブチャンネルも運営中です。ぜひチェックしてみてください！
        </p>
        <ListChannel />
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.section-top-channels {
  > .container {
    display: flex;
    justify-content: space-between;
    padding-top: 88px;
    padding-bottom: 80px;

    @include mq(md) {
      padding-top: 64px;
      padding-bottom: 88px;
    }

    > .ch-fig {
      position: relative;
      width: 46%;
      max-width: 476px;
      overflow: hidden;

      &.js-scroll {
        // opacity: 0;
        transform: translate3d(0, 24px, 0);
        transition: all 2.8s cubic-bezier(0, 0.55, 0.45, 1);

        &.js-scroll-active {
          // opacity: 1;
          transform: translate3d(0, 0, 0);
        }
      }

      @include mq(sm) {
        position: absolute;
        right: -12px;
        bottom: 340px;
        width: calc(100% + 24px);
        height: 200px;
        z-index: -1;
      }

      @include mq(xxs) {
        bottom: 348px;
      }

      > .ch-fig-img {
        position: absolute;
        right: 50%;
        bottom: 50%;
        transform: translate(50%, 50%);
        width: 100%;
        height: 100%;

        @include mq(sm) {
          height: auto;
        }
      }
    }

    > .ch-txts {
      width: 50%;
      padding-top: 16px;
      padding-bottom: 16px;

      @include mq(sm) {
        width: 100%;
        padding-top: 0;
        padding-bottom: 0;
      }

      > .ch-txt {
        margin-top: 32px;

        @include mq(sm) {
          width: 80%;
          min-width: 240px;
          margin-top: 16px;
        }
      }

      > .list {
        max-width: 400px;
        margin-top: 44px;

        @include mq(sm) {
          margin-top: 240px;
        }

        @include mq(xxs) {
          // max-width: 288px;
          margin: 240px auto 0;
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
