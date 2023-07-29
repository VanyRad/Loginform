<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-sm-4 mx-auto">
    <h2>Login</h2>
    <form @submit="login">
      <div class="mb-3">
        <label for="username" class="form-label">Логин</label>
        <input type="text" class="form-control" id="username" v-model="username" required>
      </div>
      <div class="mb-3">
        <label for="password" class="form-label">Пароль</label>
        <input type="password" class="form-control" id="password" v-model="password" required>
      </div>
      <button type="submit" class="btn btn-primary">Login</button>
    </form>
  </div>
  </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    login(event) {
      event.preventDefault();
      if (this.username === 'admin' && this.password === 'password') {
        alert('Вы успешно вошли!');
        // Здесь вы можете добавить код для перехода на другую страницу после успешной авторизации.
      } else {
        alert('Неверное имя пользователя или пароль. Пожалуйста попробуйте еще!');
      }
    }
  }
}
</script>


<style>

</style>
   