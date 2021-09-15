<template>
  <q-page class="flex flex-center" padding>
    <div class="full-width" style="max-width: 300px;">
      <h5 class="q-my-md text-center">Login</h5>
      <q-card>
        <q-card-section>
          <q-form>
            <q-input
              label="email"
              filled
              placeholder="email@example.com"
              class="q-mb-md"
            ></q-input>
            <q-input label="password" filled type="password" class="q-mb-sm"></q-input>
            <q-checkbox label="remember me" :model-value="true"></q-checkbox>
          </q-form>
        </q-card-section>
        <q-btn class="full-width" label="login" color="primary"></q-btn>
      </q-card>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "LoginPage",
};
</script>
