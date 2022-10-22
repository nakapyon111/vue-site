<template>
  <div class="content content-prof-simple">
    <figure class="prof-fig">
      <picture class="prof-fig-img">
        <img
          src="/imgs/amitysensei-icon.jpg"
          alt="amity_sensei"
          loading="lazy"
        />
      </picture>
    </figure>
    <h2 class="prof-nm txt-center">amity_sensei</h2>
    <p class="prof-position txt-center">
      アートディレクター / iPad YouTuber / olio.inc CEO
    </p>
    <p class="prof-bio">
      iPadをクリエイティブに使う方法を発信する登録者25万人超えのYouTubeチャンネルを運営中。クリエイターや企業の働き方を変えるワークデザインやコンサル業・セミナー講師なども行っている。書籍「iPadクリエイティブ」発売中。
    </p>
    <div class="sns-more">
      <ListSns class="icon-large" />
      <ButtonLink to="/about">ABOUT</ButtonLink>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.content-prof-simple {
  > .prof-fig {
    position: relative;
    display: flex;
    justify-content: center;
    width: 160px;
    margin: auto;
    border-radius: 50%;
    overflow: hidden;

    @include mq(md) {
      width: 120px;
    }

    @include mq(sm) {
      width: 100px;
    }

    @include mq(xs) {
      width: 88px;
    }

    &::before {
      content: '';
      width: 100%;
      padding-top: 100%;
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
    margin-top: 16px;
    letter-spacing: 0;

    @include mq(sm) {
      font-size: 24px;
    }
  }

  > .prof-position {
    margin-top: 14px;

    @include mq(sm) {
      font-size: 12px;
    }
  }

  > .prof-bio {
    margin-top: 8px;

    @include mq(sm) {
      margin-top: 16px;
    }

    @include mq(xxs) {
      letter-spacing: -0.01em;
    }
  }

  > .sns-more {
    display: flex;
    flex-direction: column;

    > .list {
      order: 1;
      width: 100%;
      margin-top: 16px;
      justify-content: center;

      @include mq(md) {
        order: 2;
        margin-top: 20px;
      }
    }

    > .button-link {
      order: 2;
      width: 100%;
      max-width: 200px;
      margin: 24px auto 0;

      @include mq(md) {
        order: 1;
      }
    }
  }
}
</style>
