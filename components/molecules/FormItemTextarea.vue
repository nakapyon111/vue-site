<template>
  <label class="form-item form-item-textarea">
    <textarea
      v-bind="$attrs"
      class="textarea font-futura"
      @input="$emit('input', $event.target.value)"
    ></textarea>
  </label>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.form-item-textarea {
  display: flex;

  > .textarea {
    width: 100%;
    height: 320px;
    padding: 16px;
    line-height: 1.4em;
    border: none;
    border-radius: 0;

    &::placeholder {
      color: var(--color-font-gray);
    }
  }
}
</style>
