<template>
  <div max-width="200">
    <h1 class="text-center">Get in Touch</h1>
    <p class="text-center pt-2" style="color: #fffff;">
      Please feel free to talk to us if you have any questions.
      <br />We endeavour to answer within 24 hours
    </p>
    <v-card
      outlined
      tile
      style="color: #506675; background: #fff;"
      max-width="400"
      class="mx-auto pt-3"
    >
      <v-card-text>
        <v-form class="contact-form" ref="form" @submit.prevent="sendEmail">
          <v-text-field label="Name" :rules="inputRules" outlined color="blue" name="user_name"></v-text-field>
          <v-text-field label="Email" :rules="emailRules" outlined color="blue" name="user_email"></v-text-field>
          <v-textarea label="Message" :rules="inputRules" outlined color="blue" name="message"></v-textarea>
          <div class="text-center">
            <v-btn
              class="pa-4"
              large
              text
              style="
                background-color: #10508d;
                line-height: 1;
                color: #fff;
                font-size: 12px;
              "
              outlined
              type="submit"
            >send message</v-btn>
          </div>
        </v-form>
      </v-card-text>
    </v-card>
  </div>
</template>

<script>
import emailjs from 'emailjs-com'

export default {
  data() {
    return {
      inputRules: [
        (v) => (v && v.length >= 2) || 'minimum length is 2 characters',
      ],
      emailRules: [
        (v) => !!v || 'E-mail is required',
        (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
    }
  },
  methods: {
    sendEmail(e) {
      e.preventDefault()
      if (this.$refs.form.validate()) {
        emailjs
          .sendForm(
            'mail_smtp_server',
            'template_ywbob22',
            e.target,
            'user_7ajDmDNTguP77GrIyupW3'
          )
          .then(
            (result) => {
              console.log('SUCCESS!', result.status, result.text)
              this.$swal({
                icon: 'success',
                title: 'Message sent',
                showConfirmButton: false,
                timer: 2000,
              })
            },
            (error) => {
              console.log('FAILED...', error)
              this.$swal({
                icon: 'warning',
                title: 'Message error',
                showConfirmButton: false,
                timer: 2000,
              })
            }
          )
        this.$refs.form.reset()
      }
    },
  },
}
</script>
