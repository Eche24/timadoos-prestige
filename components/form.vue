<template>
  <div max-width="200">
    <h1 class="text-center">Get in Touch</h1>
    <p class="text-center pt-2" style="color: #fffff;">
      Please feel free to talk to us if you have any questions.
      <br />We endeavour to answer within 24 hours
    </p>

    <v-card flat style="color: #506675; background: #fff;" max-width="400" class="mx-auto pt-3">
      <v-alert type="success" class="alert" v-model="alert">your message has been sent</v-alert>
      <v-card-text>
        <v-form class="px-3" ref="form">
          <v-text-field label="Name" v-model="name" :rules="inputRules" outlined color="blue"></v-text-field>

          <v-text-field label="E-mail" v-model="email" :rules="emailRules" outlined color="blue"></v-text-field>
          <v-textarea label="Message" v-model="message" :rules="inputRules" outlined color="blue"></v-textarea>
          <div class="text-center">
            <v-btn
              class="pa-4"
              color
              @click="submit"
              large
              text
              style="
                background-color: #10508d;
                font-size: 12px;
                line-height: 1;
              "
            >
              <span class>
                <a style="color: #fff; text-transform: lowercase;">Send message</a>
              </span>
            </v-btn>
          </div>
        </v-form>
      </v-card-text>
    </v-card>
  </div>
</template>
<script>
import { fireDb } from '@/plugins/firebase.js'
export default {
  data() {
    return {
      alert: false,
      name: '',
      message: '',
      inputRules: [
        (v) => (v && v.length >= 3) || 'minimum length is 3 characters',
      ],
      email: '',
      emailRules: [
        (v) => !!v || 'E-mail is required',
        (v) => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
    }
  },
  methods: {
    submit(e) {
      e.preventDefault()

      if (this.$refs.form.validate()) {
        this.alert = true
        const info = {
          name: this.name,
          email: this.email,
          message: this.message,
          date: new Date(),
        }

        fireDb
          .collection('info')
          .add(info)
          .then(() => {
            setTimeout(() => {
              this.alert = false
            }, 1000)

            this.$refs.form.reset()
          })
      }
    },
  },
}
</script>
