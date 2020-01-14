<template>
  <div>
    <v-row align="center" justify="center">
      <recaptcha @error="onError" @success="onSuccess" @expired="onExpired" />

      <v-snackbar v-model="snackbar" :multi-line="multiLine">
        {{ text }}
        <v-btn @click="snackbar = false" color="red" text>
          Close
        </v-btn>
      </v-snackbar>
    </v-row>
    <br />
  </div>
</template>

<script>
export default {
  data: () => ({
    multiLine: true,
    snackbar: false,
    text: ''
  }),
  methods: {
    showSnackbar(msg) {
      this.text = msg
      this.snackbar = true
    },
    onError(error) {
      this.showSnackbar(`reCAPTCHA Error happened ${error}`)
      this.$emit('reCaptchaSuccess', false)
    },
    onSuccess(token) {
      // TODO: don't show on snackbar
      // this.showSnackbar('ReCaptcha token:', token)
      this.$emit('reCaptchaSuccess', true)
    },
    onExpired() {
      this.showSnackbar(`reCAPTCHA Epired`)
      this.$emit('reCaptchaSuccess', false)
    }
  }
}
</script>

<style></style>
