<template>
  <section class="section section-contact-form page">
    <div class="bg bg-cover">
      <div class="bg-img"></div>
    </div>
    <div class="container">
      <h1 class="page-ttl">CONTACT</h1>
      <FormContact />
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.section-contact-form {
  padding-bottom: 96px;

  > .bg {
    > .bg-img {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background-image: url('/imgs/page/contact/amitysensei-contact-form.jpg');
      background-position: center;
      background-size: cover;
    }
  }
}
</style>
