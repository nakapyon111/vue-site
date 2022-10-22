<template>
  <section class="section section-about-profile">
    <div class="container">
      <h1 class="page-ttl">ABOUT</h1>
      <figure class="prof-fig">
        <picture class="prof-fig-img">
          <img
            src="/imgs/page/about/amitysensei-top-kv-icon.jpg"
            alt="amity?senseiのプロフィールの画像"
          />
        </picture>
      </figure>
      <h2 class="prof-nm">amity_sensei</h2>
      <p class="prof-position">
        アートディレクター / iPad YouTuber / olio.inc CEO
      </p>
      <hr class="prof-hr" />
      <p class="prof-bio prof-bio-ja">
        1993年京都生まれ。イギリスの美術大学にてデジタル&テクノロジーアートを学び、iPadでのデザイン制作活動を開始。学生のかたわら、ロンドンの日本人No.1ブロガーとしても活動。
        帰国後、2017年に外資系広告代理店に入社。その後、Adobe MAX JAPAN 2018
        スピーカー出演やYouTubeチャンネル開設を機に2019年に独立、株式会社olioを設立。
        オンラインサロン「iPadmate」の運営を経て、現在はiPadセミナー講師など、クリエイターや企業の働き方を変えるワークデザインやコンサル業を行っている。著書「iPadクリエイティブ」好評発売中。
      </p>
      <p class="prof-bio prof-bio-en">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
        veniam, quis nostrud exercitation ullamco Lorem ipsum dolor sit amet,
        consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore
        et dolore magna aliqua. Lorem ipsum dolor sit amet, consectetur
        adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore
        magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
        consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore
        et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud
        exercitation ullamco
      </p>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.section-about-profile {
  > .container {
    padding-bottom: 40px;

    > .prof-fig {
      position: relative;
      display: flex;

      &::before {
        content: '';
        width: 100%;
        padding-top: 51.851851851%;
      }

      > .prof-fig-img {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
      }
    }

    > .prof-nm {
      margin-top: 32px;
      letter-spacing: 0;
      text-align: left;

      @include mq(sm) {
        margin-top: 24px;
        font-size: 24px;
      }

      @include mq(xs) {
        text-align: center;
      }
    }

    > .prof-position {
      margin-top: 8px;
      text-align: left;

      @include mq(sm) {
        margin-top: 4px;
      }

      @include mq(xs) {
        text-align: center;
      }
    }

    > .prof-hr {
      width: 32%;
      max-width: 240px;
      min-width: 160px;
      margin-top: 32px;
      margin-bottom: 0;
      border-color: var(--color-stroke-gray);

      @include mq(sm) {
        margin-top: 24px;
      }

      @include mq(xs) {
        margin: 24px auto 0;
      }
    }

    > .prof-bio {
      max-width: 960px;
      margin-top: 40px;
      padding-right: 40px;

      @include mq(sm) {
        margin-top: 24px;
        padding-right: 0;
      }
    }
  }
}
</style>
