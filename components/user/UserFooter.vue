<template>
  <div class="container">
    <footer class="py-3 my-4">
      <ul class="nav justify-content-center border-bottom pb-3 mb-3">
        <li class="nav-item">
          <NuxtLink class="nav-link px-2 text-muted" to="/">
            Главная
          </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink class="nav-link px-2 text-muted" to="university">
            Университет
          </NuxtLink>
        </li>
        <li class="nav-item">
          <NuxtLink class="nav-link px-2 text-muted" to="learning">
            Образование
          </NuxtLink>
        </li>
        <li class="nav-item">
          <a class="nav-link px-2 text-muted" href="#">Партнёры</a>
        </li>
      </ul>
      <p class="text-center text-muted">
        © 2022 СибГУ УОЛ
      </p>
    </footer>
  </div>
</template>
<script>
export default {
  name: 'UserFooter'
}
</script>
