<template>
  <article class="page page-news-nid">
    <SectionNewsDetail :news="news" />
    <SectionNewsRecent :newses-recent="newsesRecent" />
  </article>
</template>

<script>
export default {
  data() {
    return {
      news: {
        id: 409,
        date: '2021-02-28T11:27:00',
        date_gmt: '2021-02-28T02:27:00',
        guid: {
          rendered: 'http://amitysensei.com/wp/?p=409',
        },
        modified: '2021-03-17T14:12:30',
        modified_gmt: '2021-03-17T05:12:30',
        slug: 'hello-world-10-2',
        status: 'publish',
        type: 'post',
        link: 'https://amitysensei.com/wp/uncategorized/hello-world-10-2/',
        title: {
          rendered: 'iPadセミナー「Affinity Photoを使った広告デザイン」を公開',
        },
        content: {
          rendered: `
            <p>amity_senseiの初の書籍。iPadとApple Pencilがあれば、日常がもっと鮮やかに、豊かになる」をテーマに、普通のiPad本には載ってないようなiPadチュートリアルや裏技を全190ページにわたり紹介。(約50以上のチュートリアル集)   発売前から予約が殺到し、発売初日に重版が決定。3度の重版を繰り返し現在好評発売中。</p>
            <figure class="wp-block-image size-large"><img src="/news/unnamed.jpeg" alt="" class="wp-image-444" /></figure>
            <figure class="wp-block-image size-large"><img src="/news/IMG_1258-1536x756.jpeg" alt="" class="wp-image-327" /></figure>
            <figure class="wp-block-embed is-type-video is-provider-youtube wp-block-embed-youtube wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper"><iframe loading="lazy" title="【ご報告】Today at Appleに出演します！念願のApple公式 iPadセミナーで、初めて私のアレを公開します！" width="580" height="326" src="https://www.youtube.com/embed/yQh4gC51P8g?feature=oembed" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen=""></iframe></div></figure>
          `,
          protected: false,
        },
        excerpt: {
          rendered:
            '<p>ハンバーガーを題材に、Affinity Photoを使った広告デザインについて学びます。上級者向けのアプリですが、マスターするとiPadでのデザイン・画像編集力が格段にアップします。 以下のような方々におすすめのセミナー [&hellip;]</p>\n',
          protected: false,
        },
        author: 1,
        featured_media: 444,
        comment_status: 'open',
        ping_status: 'open',
        sticky: false,
        template: '',
        format: 'standard',
        meta: [],
        categories: [1],
        tags: [],
        acf: [],
        _links: {
          self: [
            {
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/posts/409',
            },
          ],
          collection: [
            {
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/posts',
            },
          ],
          about: [
            {
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/types/post',
            },
          ],
          author: [
            {
              embeddable: true,
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/users/1',
            },
          ],
          replies: [
            {
              embeddable: true,
              href:
                'https://amitysensei.com/wp/wp-json/wp/v2/comments?post=409',
            },
          ],
          'version-history': [
            {
              count: 2,
              href:
                'https://amitysensei.com/wp/wp-json/wp/v2/posts/409/revisions',
            },
          ],
          'predecessor-version': [
            {
              id: 449,
              href:
                'https://amitysensei.com/wp/wp-json/wp/v2/posts/409/revisions/449',
            },
          ],
          'wp:featuredmedia': [
            {
              embeddable: true,
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/media/444',
            },
          ],
          'wp:attachment': [
            {
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/media?parent=409',
            },
          ],
          'wp:term': [
            {
              taxonomy: 'category',
              embeddable: true,
              href:
                'https://amitysensei.com/wp/wp-json/wp/v2/categories?post=409',
            },
            {
              taxonomy: 'post_tag',
              embeddable: true,
              href: 'https://amitysensei.com/wp/wp-json/wp/v2/tags?post=409',
            },
          ],
          curies: [
            {
              name: 'wp',
              href: 'https://api.w.org/{rel}',
              templated: true,
            },
          ],
        },
        _embedded: {
          author: [
            {
              id: 1,
              name: 'amity_sensei',
              url: 'http://amitysensei.com/wp',
              description: '',
              link: 'https://amitysensei.com/wp/author/amity_sensei/',
              slug: 'amity_sensei',
              avatar_urls: {
                24: 'https://secure.gravatar.com/avatar/192efdadd627d948928ef4b6fe5736bb?s=24&d=mm&r=g',
                48: 'https://secure.gravatar.com/avatar/192efdadd627d948928ef4b6fe5736bb?s=48&d=mm&r=g',
                96: 'https://secure.gravatar.com/avatar/192efdadd627d948928ef4b6fe5736bb?s=96&d=mm&r=g',
              },
              acf: [],
              _links: {
                self: [
                  {
                    href: 'https://amitysensei.com/wp/wp-json/wp/v2/users/1',
                  },
                ],
                collection: [
                  {
                    href: 'https://amitysensei.com/wp/wp-json/wp/v2/users',
                  },
                ],
              },
            },
          ],
          'wp:featuredmedia': [
            {
              id: 444,
              date: '2021-03-17T12:59:30',
              slug: 'unnamed',
              type: 'attachment',
              link:
                'https://amitysensei.com/wp/uncategorized/hello-world-10-2/attachment/unnamed/',
              title: {
                rendered: 'unnamed',
              },
              author: 1,
              acf: [],
              caption: { rendered: '' },
              alt_text: '',
              media_type: 'image',
              mime_type: 'image/jpeg',
              media_details: {
                width: 640,
                height: 360,
                file: '2021/03/unnamed.jpeg',
                sizes: {
                  medium: {
                    file: 'unnamed-300x169.jpeg',
                    width: 300,
                    height: 169,
                    mime_type: 'image/jpeg',
                    source_url:
                      'https://amitysensei.com/wp/wp-content/uploads/2021/03/unnamed-300x169.jpeg',
                  },
                  thumbnail: {
                    file: 'unnamed-150x150.jpeg',
                    width: 150,
                    height: 150,
                    mime_type: 'image/jpeg',
                    source_url:
                      'https://amitysensei.com/wp/wp-content/uploads/2021/03/unnamed-150x150.jpeg',
                  },
                  full: {
                    file: 'unnamed.jpeg',
                    width: 640,
                    height: 360,
                    mime_type: 'image/jpeg',
                    source_url:
                      'https://amitysensei.com/wp/wp-content/uploads/2021/03/unnamed.jpeg',
                  },
                },
                image_meta: {
                  aperture: '0',
                  credit: '',
                  camera: '',
                  caption: '',
                  created_timestamp: '0',
                  copyright: '',
                  focal_length: '0',
                  iso: '0',
                  shutter_speed: '0',
                  title: '',
                  orientation: '0',
                  keywords: [],
                },
              },
              source_url:
                'https://amitysensei.com/wp/wp-content/uploads/2021/03/unnamed.jpeg',
              _links: {
                self: [
                  {
                    href: 'https://amitysensei.com/wp/wp-json/wp/v2/media/444',
                  },
                ],
                collection: [
                  { href: 'https://amitysensei.com/wp/wp-json/wp/v2/media' },
                ],
                about: [
                  {
                    href:
                      'https://amitysensei.com/wp/wp-json/wp/v2/types/attachment',
                  },
                ],
                author: [
                  {
                    embeddable: true,
                    href: 'https://amitysensei.com/wp/wp-json/wp/v2/users/1',
                  },
                ],
                replies: [
                  {
                    embeddable: true,
                    href:
                      'https://amitysensei.com/wp/wp-json/wp/v2/comments?post=444',
                  },
                ],
              },
            },
          ],
          'wp:term': [
            [
              {
                id: 1,
                link: 'https://amitysensei.com/wp/category/uncategorized/',
                name: '未分類',
                slug: 'uncategorized',
                taxonomy: 'category',
                acf: [],
                _links: {
                  self: [
                    {
                      href:
                        'https://amitysensei.com/wp/wp-json/wp/v2/categories/1',
                    },
                  ],
                  collection: [
                    {
                      href:
                        'https://amitysensei.com/wp/wp-json/wp/v2/categories',
                    },
                  ],
                  about: [
                    {
                      href:
                        'https://amitysensei.com/wp/wp-json/wp/v2/taxonomies/category',
                    },
                  ],
                  'wp:post_type': [
                    {
                      href:
                        'https://amitysensei.com/wp/wp-json/wp/v2/posts?categories=1',
                    },
                  ],
                  curies: [
                    {
                      name: 'wp',
                      href: 'https://api.w.org/{rel}',
                      templated: true,
                    },
                  ],
                },
              },
            ],
            [],
          ],
        },
      },
      newsesRecent: [
        {
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
        {
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
        {
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
        {
          title: {
            rendered: 'Note更新。GoodNotes5をもっと使いこなす裏ワザ公開!!」',
          },
          source_url: '/imgs/page/top/work-thumb.jpg',
        },
      ],
    }
  },
}
</script>
