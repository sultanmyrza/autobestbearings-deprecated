<template>
  <v-row align="center" justify="center">
    <v-col lg="4" md="6" sm="10" xs="10">
      <v-form
        ref="form"
        @submit.prevent="submitForm"
        v-model="valid"
        :lazy-validation="lazy"
      >
        <v-text-field
          v-model="country"
          :counter="20"
          :rules="requiredRules"
          label="Country"
          required
        ></v-text-field>

        <v-text-field
          v-model="company"
          :counter="20"
          :rules="requiredRules"
          label="Company"
          required
        ></v-text-field>

        <v-text-field
          v-model="name"
          :counter="20"
          :rules="requiredRules"
          label="Name"
          required
        ></v-text-field>

        <v-text-field
          v-model="email"
          :rules="emailRules"
          label="E-mail"
          required
        ></v-text-field>

        <v-text-field
          v-model="subject"
          :counter="20"
          :rules="requiredRules"
          label="Subject"
          required
        ></v-text-field>

        <v-textarea
          :rules="requiredRules"
          v-model="message"
          label="Message"
        ></v-textarea>

        <re-captcha @reCaptchaSuccess="onReCaptchaSuccess" />

        <v-btn @click="reset" color="warning" class="mr-4">
          Reset Form
        </v-btn>

        <v-btn
          :disabled="!valid || !reCatpcha"
          @click="submitForm"
          color="success"
        >
          Submit
        </v-btn>
      </v-form>
    </v-col>
  </v-row>
</template>

<script>
import ReCaptcha from './ReCaptcha.vue'

export default {
  components: { ReCaptcha },
  data: () => ({
    valid: false,
    reCatpcha: false,
    country: '',
    company: '',
    phone: '',
    fax: '',
    subject: '',
    message: '',
    name: '',
    requiredRules: [(v) => !!v || 'required'],
    email: '',
    emailRules: [
      (v) => !!v || 'required',
      (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid'
    ],

    lazy: false
  }),

  methods: {
    onReCaptchaSuccess(success) {
      this.reCatpcha = success === true
    },
    validate() {
      if (this.$refs.form.validate()) {
        this.snackbar = true
      }
    },
    reset() {
      this.$refs.form.reset()
    },
    resetValidation() {
      this.$refs.form.resetValidation()
    },
    submitForm() {
      // TODO send email to our server
    }
  }
}
</script>
