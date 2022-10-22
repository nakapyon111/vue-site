<template>
  <article class="page page-index">
    <SectionTopKv />
    <div class="sections">
      <SectionTopAboutNews :newses="newses" />
      <SectionTopWorks :works="works" />
      <SectionTopChannels />
      <SectionTopSns />
    </div>
  </article>
</template>

<script>
export default {
  data() {
    return {
      newses: [
        {
          text: '',
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
        {
          text: '',
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
        {
          text: '',
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
      ],
      udemy: [],
      works: [
        {
          text: '',
          title: {
            rendered: '書籍 iPadクリエイティブ',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
          acf: {
            client: 'KADOKOKAWA',
          },
          date: '2020.12.01',
        },
        {
          text: '',
          title: {
            rendered: '書籍 iPadクリエイティブ',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
          acf: {
            client: 'KADOKOKAWA',
          },
          date: '2020.12.01',
        },
        {
          text: '',
          title: {
            rendered: '書籍 iPadクリエイティブ',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
          acf: {
            client: 'KADOKOKAWA',
          },
          date: '2020.12.01',
        },
        {
          text: '',
          title: {
            rendered: '書籍 iPadクリエイティブ',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
          acf: {
            client: 'KADOKOKAWA',
          },
          date: '2020.12.01',
        },
        {
          text: '',
          title: {
            rendered: '書籍 iPadクリエイティブ',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
          acf: {
            client: 'KADOKOKAWA',
          },
          date: '2020.12.01',
        },
        {
          text: '',
          title: {
            rendered: '書籍 iPadクリエイティブ',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
          acf: {
            client: 'KADOKOKAWA',
          },
          date: '2020.12.01',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
.page-index {
  padding-top: 0;
  padding-bottom: 0;

  > .sections {
    position: relative;
    padding-top: 80px;
    padding-bottom: 88px;
    background-color: var(--color-bg-default);

    @include mq(sm) {
      padding-bottom: 72px;
    }
  }
}

// .js-header-logo.nuxt-link-exact-active {
//   opacity: 0;
//   transition: all 0.64s cubic-bezier(0, 0.55, 0.45, 1);

//   &.js-header-logo-active {
//     opacity: 1;
//   }
// }
</style>
