<script setup></script>

<template>
  <section>
    <div class="container w-75 bg-primary mt-5 mb-4 rounded shadow-lg">
      <div class="row aling-item-stretch">
        <div class="col bg d-none d-lg-block col-md-5 col-lg-5 col-xl-6 rounded"></div>
        <div class="col bg-white p-4 rounded-end">
          <div class="text-end">
            <img src="../../assets/static/icon/IconLogin.svg" width="100px" height="120px" />
          </div>
          <div v-if="error != ''" class="alert alert-danger" role="alert">
            <p>{{ error }}</p>
          </div>
          <h1 class="fw-bold text-center py-5">WELCOME</h1>
          <form @submit.prevent="handleLogin">
            <div class="mb-4">
              <label for="email" class="form-label">Email</label>
              <input
                v-model="email"
                type="email"
                placeholder="Email"
                class="form-control"
                required
              />
            </div>
            <div class="mb-4">
              <label for="password" class="form-label">Password</label>
              <input
                type="password"
                v-model="password"
                placeholder="Password"
                class="form-control"
                required
              />
            </div>
            <div class="d-grid">
              <button type="submit" class="btn btn-primary">Login</button>
            </div>
          </form>
          <div class="mb-7">
            <a href="#" class="class-form">Create Account</a>
          </div>
          <div class="mb-7">
            <a href="#" class="class-form">Recover Key</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
body {
  background: #fafafa;
}

.bg {
  background-image: url(https://nextday-software.com/wp-content/uploads/2023/04/problemas-contables-empresas.jpg);
  background-position: center center;
}
</style>
