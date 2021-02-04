<template>
  <v-row class="mt-6">
    <v-col cols="3"></v-col>
    <v-col cols="6">
      <v-card>
        <v-card-title>
          <h1 class="display-1">Kullanıcı Girişi Vuetify</h1>
        </v-card-title>
        <v-card-text>
          <v-form>
            <v-text-field
              label="Kullanıcı Adı"
              prepend-icon="mdi-account-circle"
            >
            </v-text-field>
            <v-text-field
              :type="showPassword ? 'text' : 'password'"
              label="Şifre"
              prepend-icon="mdi-lock"
              :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
              @click:append="showPassword = !showPassword"
            ></v-text-field>
          </v-form>
        </v-card-text>
        <v-divider></v-divider>
        <v-card-actions>
          <v-btn color="success">Üye Ol</v-btn>
          <v-spacer></v-spacer>
          <v-btn color="info"
            ><span class="font-weight-regular"> Giriş </span></v-btn
          >
        </v-card-actions>
      </v-card>
    </v-col>
    <v-col cols="3"></v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({ showPassword: false })
};
</script>

<style></style>
