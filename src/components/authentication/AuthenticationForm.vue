<template>
  <v-container fluid fill-height>
    <v-layout align-center justify-center>
      <v-flex xs12 sm8 md4>
        <v-card elevation="2">
          <v-toolbar elevation="0" dark color="primary">
            <v-toolbar-title>Login</v-toolbar-title>
          </v-toolbar>
          <v-card-text>
            <v-form>
              <v-text-field
                :v-model="credential.email"
                prepend-icon="mdi-account"
                name="login"
                label="Email"
                type="text"
              ></v-text-field>
              <v-text-field
                :v-model="credential.password"
                prepend-icon="mdi-lock"
                name="password"
                label="Password"
                type="password"
              ></v-text-field>
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" dark>
              <span class="mx-2">Login</span>
              <v-icon>mdi-login</v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script lang="ts">
import { Credential } from '@/models/authentication'
import { EMPTY_CREDENTIAL } from '@/constants/authentication'
import { Component, Vue } from 'vue-property-decorator'

@Component
export default class AuthenticationForm extends Vue {
  showPassword = false
  credential: Credential = EMPTY_CREDENTIAL
}
</script>
