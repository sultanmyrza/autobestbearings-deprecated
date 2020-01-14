<template>
  <v-layout>
    <v-flex class="text-center">
      <blockquote class="blockquote">
        &#8220;Please feel free to leave your messages here. We will reply to
        you as soon as possible according to the contact messages you
        left..&#8221;
        <footer>
          <small>
            <em>&mdash; manager of AUTO BEST BEARINGS CO., LTD</em>
          </small>
        </footer>
      </blockquote>
      <contact-form />
    </v-flex>
  </v-layout>
</template>

<script>
import ContactForm from '../components/ContactForm.vue'
export default {
  components: { ContactForm },
  data: () => ({
    valid: true,
    name: '',
    nameRules: [
      (v) => !!v || 'Name is required',
      (v) => (v && v.length <= 10) || 'Name must be less than 10 characters'
    ],
    email: '',
    emailRules: [
      (v) => !!v || 'E-mail is required',
      (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid'
    ],
    select: null,
    items: ['Item 1', 'Item 2', 'Item 3', 'Item 4'],
    checkbox: false,
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
    }
  }
}
</script>
