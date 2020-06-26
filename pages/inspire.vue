<template>
  <v-layout>
    <v-flex class="text-center">
      <img src="/v.png" alt="Vuetify.js" class="mb-5" />
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;{{ firstUser.name }}</em>
          </small>
        </footer>
      </blockquote>
    </v-flex>
  </v-layout>
</template>

<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

interface User {
  name: string
}

@Component
export default class TestClass extends Vue {
  mounted() {
    this.testFunc()
  }

  firstUser: User = {
    name: '',
  }

  testFunc() {
    this.firstUser.name = 'firstUser'
  }
}
</script>
