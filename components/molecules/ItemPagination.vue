<template>
  <ul v-if="totalPage > 1" class="item item-pagination">
    <li class="item">
      <nuxt-link
        :to="`?${query}=${now - 1 || 1}`"
        :class="{ inactive: now === 1 }"
        class="item-link prev"
      >
        <svg viewBox="0 0 24 24" class="icon">
          <use xlink:href="#i-arrow" />
        </svg>
      </nuxt-link>
    </li>
    <li class="item">
      <nuxt-link
        :to="`?${query}=1`"
        :class="{ current: now === 1 }"
        class="item-link"
      >
        1
      </nuxt-link>
    </li>
    <template v-if="totalPage >= 2">
      <template v-if="totalPage <= 5">
        <li class="item">
          <nuxt-link
            :to="`?${query}=2`"
            :class="{ current: now === 2 }"
            class="item-link"
          >
            2
          </nuxt-link>
        </li>
        <template v-if="totalPage >= 3">
          <li class="item">
            <nuxt-link
              :to="`?${query}=3`"
              :class="{ current: now === 3 }"
              class="item-link"
            >
              3
            </nuxt-link>
          </li>
        </template>
        <template v-if="totalPage >= 4">
          <li class="item">
            <nuxt-link
              :to="`?${query}=4`"
              :class="{ current: now === 4 }"
              class="item-link"
            >
              4
            </nuxt-link>
          </li>
        </template>
        <template v-if="totalPage >= 5">
          <li class="item">
            <nuxt-link
              :to="`?${query}=5`"
              :class="{ current: now === 5 }"
              class="item-link"
            >
              5
            </nuxt-link>
          </li>
        </template>
      </template>
      <template v-else>
        <template v-if="now < 3">
          <li class="item">
            <nuxt-link
              :to="`?${query}=2`"
              :class="{ current: now === 2 }"
              class="item-link"
            >
              2
            </nuxt-link>
          </li>
          <li class="item">
            <nuxt-link
              :to="`?${query}=3`"
              :class="{ current: now === 3 }"
              class="item-link"
            >
              3
            </nuxt-link>
          </li>
          <li class="item">
            <p class="item-dot item-link">...</p>
          </li>
        </template>
        <template v-else-if="totalPage - now < 2">
          <li class="item">
            <p class="item-dot item-link">...</p>
          </li>
          <li class="item">
            <nuxt-link
              :to="`?${query}=totalPage - 2`"
              :class="{ current: now === totalPage - 2 }"
              class="item-link"
            >
              {{ totalPage - 2 }}
            </nuxt-link>
          </li>
          <li class="item">
            <nuxt-link
              :to="`?${query}=totalPage - 1`"
              :class="{ current: now === totalPage - 1 }"
              class="item-link"
            >
              {{ totalPage - 1 }}
            </nuxt-link>
          </li>
        </template>
        <template v-else>
          <li v-if="now > 3" class="item">
            <p class="item-dot item-link">...</p>
          </li>
          <li class="item">
            <nuxt-link :to="`?${query}=${now - 1}`" class="item-link">
              {{ now - 1 }}
            </nuxt-link>
          </li>
          <li class="item">
            <nuxt-link :to="`?${query}=${now}`" class="item-link current">
              {{ now }}
            </nuxt-link>
          </li>
          <li class="item">
            <nuxt-link :to="`?${query}=${now + 1}`" class="item-link">
              {{ now + 1 }}
            </nuxt-link>
          </li>
          <li v-if="now > 3" class="item">
            <p class="item-dot item-link">...</p>
          </li>
        </template>
        <li class="item">
          <nuxt-link
            :to="`?${query}=${totalPage}`"
            :class="{ current: now === totalPage }"
            class="item-link"
          >
            {{ totalPage }}
          </nuxt-link>
        </li>
      </template>
    </template>
    <li class="item">
      <nuxt-link
        :to="`?${query}=${now + 1 <= totalPage ? now + 1 : totalPage}`"
        :class="{ inactive: now === totalPage }"
        class="item-link next"
      >
        <svg viewBox="0 0 24 24" class="icon">
          <use xlink:href="#i-arrow" />
        </svg>
      </nuxt-link>
    </li>
  </ul>
</template>

<script>
export default {
  props: {
    totalPage: {
      type: Number,
      required: true,
    },
    query: {
      type: String,
      required: true,
    },
    now: {
      type: Number,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.item-pagination {
  display: flex;
  justify-content: center;
  align-items: center;

  > .item {
    margin: 0 6px;

    > .item-link {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 40px;
      height: 40px;
      background-color: var(--color-bg-gray);
      opacity: 1;
      transition: all 0.024s linear;

      &:hover {
        opacity: 0.64;
      }

      @include mq(sm) {
        width: 32px;
        height: 32px;
      }

      > .icon {
        width: 24px;
      }

      &.current {
        color: var(--color-font-white);
        background-color: var(--color-bg-black);
      }

      &.inactive {
        opacity: 0;
      }

      &.item-dot,
      &.prev,
      &.next {
        background-color: transparent;
      }

      &.prev {
        > .icon {
          transform: scale(-1, 1);
        }
      }
    }
  }
}
</style>
