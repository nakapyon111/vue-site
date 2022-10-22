<template>
  <div class="section section-top-sns">
    <div class="container">
      <section class="sns sns-insta">
        <div class="container">
          <h2 class="sns-ttl">
            <svg viewBox="0 0 24 24" class="sns-icon">
              <use xlink:href="#i-instagram" />
            </svg>
          </h2>
          <ListSnsImg :sns="instagram" />
          <ButtonLinkBlank href="https://www.instagram.com/amity_sensei/">
            INSTAGRAM</ButtonLinkBlank
          >
        </div>
      </section>
      <section class="sns sns-shop">
        <div class="container">
          <h2 class="sns-ttl">
            <svg viewBox="0 0 24 24" class="sns-icon">
              <use xlink:href="#i-shop" />
            </svg>
          </h2>
          <ListSnsImg :sns="shop" />
          <ButtonLinkBlank href="https://amity-sensei.stores.jp/">
            SHOP MORE
          </ButtonLinkBlank>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      instagram: [
        {
          href: 'https://www.instagram.com/p/CGykTWGDaix/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム１',
        },
        {
          href: 'https://www.instagram.com/p/CGtUxkBDEzJ/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム２',
        },
        {
          href: 'https://www.instagram.com/p/B7xi_yhlmLQ/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム３',
        },
        {
          href: 'https://www.instagram.com/p/CGjdp7vDEyz/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム４',
        },
        {
          href: 'https://www.instagram.com/p/CGgnKshjN7b/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム５',
        },
        {
          href: 'https://www.instagram.com/p/B0XyBjgAK3Z/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム６',
        },
        {
          href: 'https://www.instagram.com/p/CGY34fRjCd-/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム７',
        },
        {
          href: 'https://www.instagram.com/p/Bzuf6R_gsL8/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム８',
        },
        {
          href: 'https://www.instagram.com/p/B0fvVgbgaqw/',
          img: '/imgs/page/top/amitysensei-top-instagram.jpg',
          alt: 'amity_senseiのインスタグラム９',
        },
      ],

      shop: [
        {
          href:
            'https://amity-sensei.stores.jp/items/5cf4ab3aadb2a14721a54ad5/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ１',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5fc097ecdf5159329dd1fe35/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ２',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5cc02bf40b921104c346bcac/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ３',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5cc011ebadb2a137e4f32da4/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ４',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5e11a2fd6c7d632fbb60ff70/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ５',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5ed344bc55fa032e32c06a3e/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ６',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5ed3447e34ef0138b5594215/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ７',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5eb3aae972b9116c9aa6c706/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ８',
        },
        {
          href:
            'https://amity-sensei.stores.jp/items/5eb3b35855fa0345bb05c89f/',
          img: '/imgs/page/top/amitysensei-top-store.jpg',
          alt: 'amity_senseiのショップ９',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.section-top-sns {
  @include mq(sm) {
    padding: 0;
  }

  > .container {
    display: flex;
    justify-content: space-between;
    padding-top: 88px;

    @include mq(sm) {
      display: block;
      padding-top: 0;
    }

    > .sns {
      width: 49%;
      max-width: 520px;
      padding: 0 24px;
      background-color: var(--color-bg-gray);

      @include mq(sm) {
        width: 100%;
        max-width: none;
        padding: 0 26px;
      }

      > .container {
        max-width: 432px;
        padding-top: 40px;
        padding-bottom: 56px;

        @include mq(sm) {
          max-width: 360px;
          padding-top: 64px;
          padding-bottom: 80px;
        }

        > .sns-ttl {
          display: flex;
          justify-content: center;

          > .sns-icon {
            width: 48px;

            @include mq(sm) {
              width: 40px;
            }
          }
        }

        > .list {
          margin-top: 32px;

          @include mq(sm) {
            margin-top: 24px;
          }
        }

        > .button {
          max-width: 200px;
          margin: 32px auto 0;
        }
      }

      &.sns-shop {
        @include mq(sm) {
          background-color: transparent;
        }

        > .container {
          @include mq(sm) {
            padding-bottom: 0;
          }
        }
      }
    }
  }
}
</style>
