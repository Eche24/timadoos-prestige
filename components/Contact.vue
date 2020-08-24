<template>
  <v-container fluid class="pa-4">
    <v-layout row justify-center fill-height class="pt-5" align-center>
      <v-flex xs10 md5 sm5 lg5>
        <img
          src="https://res.cloudinary.com/ds4yhjjq8/image/upload/v1597966964/timadoos/Surveillance_re_8tkl_memznq.svg"
          width="90%"
        />
      </v-flex>
      <v-flex xs10 md5 sm5 lg5>
        <Form />
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
import Form from '../components/form'
export default {
  components: {
    Form,
  },
}
</script>