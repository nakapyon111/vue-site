<template>
  <section id="kv" class="section section-top-kv">
    <h1 class="page-ttl">amity_senseiのコーポレートサイト</h1>
    <div class="bg">
      <div class="bg-img"></div>
    </div>
    <div class="container">
      <svg viewBox="0 0 166 56" class="logo-img">
        <use xlink:href="#i-logo" />
      </svg>
    </div>
  </section>
</template>

<script>
export default {
  mounted() {
    const el = document.getElementById('kv')
    const children = el.children
    el.style.height = window.innerHeight + 'px'
    children.forEach((child) => {
      child.style.height = window.innerHeight + 'px'
    })
  },
}
</script>

<style lang="scss" scoped>
.section-top-kv {
  position: relative;

  > .page-ttl {
    position: relative;
    z-index: -1;
  }

  > .bg {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;

    > .bg-img {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background-image: url('/imgs/page/top/amitysensei-top-kv-icon.jpg');
      background-position: center;
      background-size: cover;

      @include mq(xs) {
        transform: scale(1.08);
        background-position: 8% -24px;
      }
    }
  }

  > .container {
    position: fixed;
    top: 0;
    right: 0;
    left: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    max-width: none;

    > .logo-img {
      width: 88%;
      max-width: 400px;
      fill: #fff;
    }
  }
}
</style>
