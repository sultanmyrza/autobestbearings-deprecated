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
  components: { ContactForm }
}
</script>
