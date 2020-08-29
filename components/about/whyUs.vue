<template>
  <v-container fluid>
    <v-layout row wrap justify-center align-center fill-height>
      <v-flex xs12 md10 sm10 lg10>
        <v-card class="pa-5 mt-3" flat>
          <v-card-title class="pt-5">
            <h2>Timadoos prestige limited– Independent security advisers</h2>
          </v-card-title>
          <v-card-subtitle class="subtitle">
            <h3>
              <span style="color: #003366;">
                If the safety and security of your people and property is important to you, then you need to find the right people to advise you.
                And&nbsp;if you are just starting out, you might not know where to go for help. &nbsp;We can point you in the right direction.
              </span>
            </h3>
          </v-card-subtitle>
          <v-card-text class="text">
            <p>
              <b>Timadoos prestige limited</b> are&nbsp;
              <strong>trusted security advisers</strong>&nbsp;specialising in
              <strong>designing and delivering customised security solutions and strategies</strong>
              <span style="text-decoration: underline;">in the following sectors</span>:
            </p>
            <v-list-item v-for="card in cards" :key="card.title">
              <v-list-item-content>
                <v-list-item-subtitle>{{card.title}}</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
            <p>
              Our 5+ years of security experience across many diverse industries and working with hundreds of clients, enables Timadoos prestige limited
              <strong>security consultants</strong> to provide
              <strong>specialised security advice</strong> to meet the specific needs and environment of any business. Our expertise is solving complex security challenges.
            </p>

            <p>Our work ranges from small consulting projects right through to managing large, complex multi-sites. With national delivery capability, we have the resources, skills and commitment to serve any security needs regardless of complexity or scale.</p>

            <p>
              At
              <b>Timadoos prestige limited</b>, we are all about the
              <strong>project and project outcomes</strong>. Our individual approach and personalised attention to every project ensures that the right solution will be designed and delivered on time, to specification and within budget.
            </p>
            <p>
              <strong>So whether you are looking for a security consultant or you just need advice,</strong> education through resources and advice is a big part of what we do, feel free to
              <a
                href="/contact/"
              >call</a> or
              <a href="/contact">email</a> us and we can help you find the answers you are looking for.
            </p>
          </v-card-text>
          <v-card-subtitle>
            <h2 style="padding-top: 1em;">Why work with Timadoos prestige limited?</h2>
            <ul class="content-list">
              <li>
                We are
                <strong>truly passionate</strong> about security, so much so, we’ve been told our passion is infectious.
              </li>
              <li>
                We offer a
                <strong>fixed project fee</strong> regardless of complexity. Even if your project exceeds the anticipated hours, we will never charge more than what was agreed to.
              </li>
              <li>
                We give every client the
                <strong>same attention</strong> regardless of size.
              </li>
              <li>
                All our projects are
                <strong>followed up with 6 and 12 monthly operational checks</strong> of the entire installation.
              </li>
              <li>
                <strong>Our clients are forever.</strong> You can contact us years after a project has ended for advice and support.
              </li>
              <li>
                We are
                <strong>on call 24/7.</strong>
              </li>
              <li>
                Unlike most other security advisories, you will only have
                <strong>one point of contact</strong> throughout your entire project ensuring a seamless delivery process.
              </li>
            </ul>
          </v-card-subtitle>
          <!-- <v-card-actions
            style="color: #fff; margin-top: 1em;font-size: 1.35em; text-transform: uppercase;">
            <v-btn large style="background: #426288;" outlined> contact us</v-btn>
          </v-card-actions>-->
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    length: 11,
    onboarding: 0,
    cards: [
      {
        title: 'CCTV INSTALLATION',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'FIRE SECURITY',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'INVERTERS',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'SOLAR PANELS INSTALLATION',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'ALL-IN-ONE SOLAR STREET LIGHT',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'ELECTRIC FENCE',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'NETWORK INFRASTRUCTURE DEPLOYMENT',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'SOFTWARE DEVELOPMENT',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'AUTOMATED SYSTEMS',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
      {
        title: 'INTERCOM',
        info:
          'Lorem ipsum dolor sit amet consectetur adipisicing elit. Molestiae ipsa atque architecto expedita provident.',
      },
    ],
  }),
}
</script>

<style scoped>
.subtitle h3 {
  font-size: 1.3em;
  letter-spacing: 0.01em;
  padding: 0.7em 0 0.9em 0;
  line-height: 1.4em;
  font-weight: 400;
}
.text p {
  margin: 0 0 1em 0;
  font-size: 1.2em;
  line-height: 1.8em;
}
.content-list li {
  margin: 0 0 0.3em 0;
  font-size: 1.15em;
  line-height: 1.8em;
}
h2 {
  font-size: 1.4em;
  letter-spacing: 0.01em;
  padding: 0.7em 0 0.7em 0;
  line-height: 1.4em;
  font-weight: 400;
  color: #38506d;
}
</style>