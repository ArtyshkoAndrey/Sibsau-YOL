<template>
  <div class="row justify-content-center min-vh-100 align-items-center">
    <div class="col-6">
      <form>
        <div class="mb-3">
          <label for="exampleInputEmail1" class="form-label">Email</label>
          <input id="exampleInputEmail1" type="email" class="form-control" aria-describedby="emailHelp">
          <div id="emailHelp" class="form-text">
            Мы используем Email только вкачестве аутентификации, и не передаём третьим лицам
          </div>
        </div>
        <div class="mb-3">
          <label for="exampleInputPassword1" class="form-label">Пароль</label>
          <input id="exampleInputPassword1" type="password" class="form-control">
        </div>
        <div class="mb-3 form-check">
          <input id="exampleCheck1" type="checkbox" class="form-check-input">
          <label class="form-check-label" for="exampleCheck1">Запомнить пароль</label>
        </div>
        <div class="row">
          <div class="col-12 col-md-auto me-auto">
            <button type="button" class="btn btn-primary px-4">
              Войти
            </button>
          </div>
          <div class="col-12 col-md-auto ms-auto">
            <NuxtLink to="/" class="btn btn-dark">
              На главную
            </NuxtLink>
          </div>
        </div>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AuthPage'
}
</script>

<style scoped lang="scss">
input, a, button, .form-check-input {
  border-radius: 0;
}
</style>
