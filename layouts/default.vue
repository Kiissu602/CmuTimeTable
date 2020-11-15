<template>
  <v-app light>
    <v-app-bar fixed app>
      <v-list nav>
        <v-list-item to="/" link exact color="primary">
          <v-list-item-action>
            <v-icon>mdi-home</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="'CMU TimeTable'" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-list nav>
        <v-list-item to="/timetable" link exact color="primary">
          <v-list-item-action>
            <v-icon>mdi-timetable</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="'ตารางเรียน'" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
      <v-spacer></v-spacer>
      <v-btn depressed color="accent" to="/login"
        ><v-icon>mdi-login-variant</v-icon> Login
      </v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/',
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire',
        },
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'CMU TimeTable',
    }
  },
  methods: {
    home() {
      this.$router.push('/')
    },
  },
}
</script>
