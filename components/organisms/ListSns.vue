<template>
  <ul class="list list-sns">
    <li v-for="s in snsList" :key="s.icon" class="sns">
      <a :href="s.href" target="_blank" class="sns-link">
        <svg viewBox="0 0 24 24" class="sns-icon">
          <use :xlink:href="s.icon" />
        </svg>
      </a>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      snsList: [
        {
          label: 'YouTube',
          icon: '#i-youtube',
          href: 'https://www.youtube.com/channel/UCcXtyjK8wagT5LWS5bBgPPQ',
        },
        {
          label: 'Twitter',
          icon: '#i-twitter',
          href: 'https://twitter.com/amity_sensei',
        },
        {
          label: 'Instagram',
          icon: '#i-instagram',
          href: 'https://www.instagram.com/amity_sensei/',
        },
        {
          label: 'facebook',
          icon: '#i-facebook',
          href:
            'https://www.facebook.com/profile.php?id=113971883336522&ref=br_rs',
        },
        {
          label: 'note',
          icon: '#i-note',
          href: 'https://note.com/ipadmate',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scopeds>
.list-sns {
  display: flex;
  margin-left: 2px;

  > .sns {
    margin-right: 2px;

    > .sns-link {
      padding: 8px;

      > .sns-icon {
        width: 24px;
        fill: var(--color-icon-default);
        transition: all 0.024s linear;
      }

      &:hover {
        > .sns-icon {
          fill: var(--color-icon-black-64);
        }
      }
    }
  }

  &.icon-large {
    > .sns {
      > .sns-link {
        > .sns-icon {
          width: 32px;

          @include mq(sm) {
            width: 24px;
          }
        }
      }
    }
  }
}
</style>
