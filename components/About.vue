<template>
  <v-container fluid>
    <v-layout row justify-center align-center fill-height wrap class="pa-4">
      <v-flex xs12 md10 lg10 sm10>
        <v-card flat max-width="700">
          <h2 class="pa-2">about us</h2>
          <v-card-text>
            <h3 style="color: #38506d;">Timadoos Prestige limited– Independent security advisers</h3>
            <p>
              If the safety and security of your people and property is important to you, then you need to find the right people to advise you.
              And&nbsp;if you are just starting out, you might not know where to go for help. &nbsp;We can point you in the right direction.
            </p>
          </v-card-text>
          <v-card-actions class="launch-wrap">
            <a href="/about" target="_blank" rel="noopener noreferrer">Read more</a>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<style scoped>
.launch-wrap a {
  color: #333;
  min-width: 12em;
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding: 0.4em 1em;
}
.launch-wrap a::after {
  content: ' →';
}

</style>