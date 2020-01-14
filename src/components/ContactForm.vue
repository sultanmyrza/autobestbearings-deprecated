<template>
  <v-row align="center" justify="center">
    <v-col lg="4" md="6" sm="10" xs="10">
      <v-form ref="form" v-model="valid" :lazy-validation="lazy">
        <v-text-field
          v-model="country"
          :counter="20"
          :rules="nameRules"
          label="Country"
          required
        ></v-text-field>

        <v-text-field
          v-model="company"
          :counter="20"
          :rules="nameRules"
          label="Company"
          required
        ></v-text-field>

        <v-text-field
          v-model="name"
          :counter="20"
          :rules="nameRules"
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
          :rules="nameRules"
          label="Subject"
          required
        ></v-text-field>

        <v-textarea v-model="message" label="Message"></v-textarea>

        <v-btn @click="reset" color="warning" class="mr-4">
          Reset Form
        </v-btn>

        <v-btn @click="submitForm" color="success">
          Submit
        </v-btn>
      </v-form>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    valid: true,
    country: '',
    company: '',
    phone: '',
    fax: '',
    subject: '',
    message: '',
    name: '',
    nameRules: [
      (v) => !!v || 'required',
      (v) => (v && v.length <= 20) || 'Name must be less than 20 characters'
    ],
    email: '',
    emailRules: [
      (v) => !!v || 'required',
      (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid'
    ],

    lazy: false
  }),

  methods: {
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
