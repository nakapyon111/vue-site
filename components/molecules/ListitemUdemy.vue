<template>
  <li class="list-item list-item-udemy"></li>
</template>

<script>
export default {
  props: {
    udemy: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.list-item-udemy {
  > .udemy-link {
    display: flex;
    flex-direction: column;
    height: 100%;

    > .udemy-fig {
      position: relative;
      display: flex;
      width: 100%;
      max-height: 447px;
      overflow: hidden;

      &::before {
        content: '';
        width: 100%;
        padding-top: 56.25%;
      }

      > .udemy-fig-img {
        position: absolute;
        top: 0;
        right: 0;
        bottom: 0;
        left: 0;
        transform: scale(1);
        transition: all 0.16s cubic-bezier(0.11, 0, 0.5, 0);
      }
    }

    > .udemy-info {
      flex: 1;
      padding: 14px 16px;
      background-color: var(--color-bg-default);

      @include mq(sm) {
        padding: 10px 12px;
      }

      > .udemy-info-cont {
        display: flex;
        flex-direction: column;
        height: 100%;

        > .udemy-app,
        > .udemy-ttl,
        > .udemy-teacher {
          line-height: 1.4em;
        }

        > .udemy-app {
          font-size: 10px;
        }

        > .udemy-ttl {
          flex: 1;
          min-height: 4.2em;
          margin-top: 2px;
          font-size: 14px;
        }

        > .udemy-teacher {
          margin-top: 4px;
          font-size: 10px;
        }
      }
    }

    &:hover {
      > .udemy-fig {
        > .udemy-fig-img {
          transform: scale(1.08);
        }
      }
    }
  }
}
</style>
