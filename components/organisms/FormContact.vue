<template>
  <form
    class="form form-contact"
    action="https://docs.google.com/forms/u/0/d/e/1FAIpQLScrqZh2I1B1yfAZBurNKB70sPLKe4G1YUu1pKTPJdH6u1P6lg/formResponse"
    target="hideResult"
  >
    <FormItemInput
      v-model="form.name"
      placeholder="Name*"
      name="entry.1863909335"
      required
    />
    <FormItemInput
      v-model="form.email"
      type="email"
      placeholder="Email*"
      name="entry.1432779352"
      required
    />
    <FormItemInput
      v-model="form.tel"
      type="tel"
      placeholder="Phone Number"
      name="entry.1607671142"
    />
    <FormItemInput
      v-model="form.title"
      placeholder="Title"
      name="entry.1470721045"
    />
    <FormItemTextarea
      v-model="form.message"
      placeholder="Message*"
      name="entry.590995856"
      required
    />
    <div class="btn">
      <div v-show="isSending" class="loader">
        <div class="loader-dot"></div>
        <div class="loader-dot"></div>
        <div class="loader-dot"></div>
      </div>
      <FormItemButton
        type="submit"
        :disabled="status === 'success'"
        @click="submitForm()"
        >SUBMIT</FormItemButton
      >
      <div class="msg txt-right">
        <p v-if="status === 'success'" class="msg-txt">Thanks!</p>
        <p v-if="status === 'error'" class="msg-txt">
          エラーが発生しました。もう一度送信してください。
        </p>
      </div>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      isSending: false,

      status: '',

      form: {
        name: '',
        email: '',
        tel: '',
        title: '',
        message: '',
      },

      formInfo: {
        action:
          'https://docs.google.com/forms/u/0/d/e/1FAIpQLSeNT5Ym20DqnoiWaeO7oYfnyxnvj0yokVyet1_-lU5ABETXww/formResponse',
        name: 'entry.841138565',
        email: 'entry.691828837',
        tel: 'entry.285746427',
        title: 'entry.1035962874',
        message: 'entry.1263499542',
      },
    }
  },
  methods: {
    submitForm() {
      if (this.form.name && this.form.email && this.form.message) {
        this.isSending = true

        const submitParams = new FormData()

        Object.keys(this.form).forEach((key) => {
          // @ts-ignore
          submitParams.append(this.formInfo[key], this.form[key])
        })

        const CORS_PROXY = 'https://cors-anywhere.herokuapp.com/'
        const GOOGLE_FORM_ACTION = this.formInfo.action

        this.$axios
          .post(CORS_PROXY + GOOGLE_FORM_ACTION, submitParams)
          .then(() => {
            this.isSending = false
            this.status = 'success'
          })
          .catch((e) => {
            console.warn(e) // eslint-disable-line
            this.isSending = false
            this.status = 'error'
          })

        setTimeout(() => {
          this.isSending = false
          this.status = 'success'
        }, 2400)
      }
    },
  },
}
</script>

<style lang="scss">
.form-contact {
  position: relative;

  > .form-item {
    margin-top: 16px;
  }

  > .btn {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    margin-top: 32px;

    @include mq(xs) {
      flex-direction: row-reverse;
    }

    > .loader {
      position: relative;
      display: flex;
      width: 32px;
      height: 32px;
      margin-right: 24px;
      margin-left: 0;

      @include mq(xs) {
        margin-right: 0;
        margin-left: 24px;
      }

      > .loader-dot {
        position: absolute;
        top: 50%;
        display: flex;
        background-color: var(--color-icon-default);
        border-radius: 50%;
        animation: loading 1.2s infinite ease-in-out both;

        &:nth-child(1) {
          left: 4%;
          transform: translate(-50%, -50%);
          animation-delay: -0.136s;
        }

        &:nth-child(2) {
          left: 50%;
          transform: translate(-50%, -50%);
        }

        &:nth-child(3) {
          left: 96%;
          transform: translate(-50%, -50%);
          animation-delay: 0.136s;
        }

        @keyframes loading {
          0%,
          80%,
          100% {
            width: 0;
            height: 0;
          }
          40% {
            width: 12px;
            height: 12px;
          }
        }
      }
    }

    > .form-item-button {
      display: block;
      max-width: 200px;
    }
  }

  > .msg {
    position: absolute;
    right: 0;
    top: 100%;
    max-width: 100%;
    padding: 8px 16px;
    background-color: var(--color-bg-default);
  }

  > *:first-child {
    margin-top: 0;
  }
}
</style>
