<template>
  <nav class="navbar fixed-top navbar-expand-lg navbar-light bg-light border-bottom border-1">
    <div class="container-fluid">
      <NuxtLink class="navbar-brand ms-5 me-5 d-flex" to="/">
        <img alt="logo" class="img-fluid logo" src="@/static/logo.svg">
      </NuxtLink>
      <button
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
        class="navbar-toggler"
        data-bs-target="#navbarSupportedContent"
        data-bs-toggle="collapse"
        type="button"
      >
        <span class="navbar-toggler-icon" />
      </button>
      <div id="navbarSupportedContent" class="collapse navbar-collapse flex-column">
        <ul id="second-ul" class="navbar-nav me-auto mb-0 mb-lg-0">
          <li v-for="m in second_menu" :key="m.title" :class="m.dropdown ? 'dropdown' : null" class="nav-item">
            <NuxtLink v-if="!m.dropdown" :to="m.path" active-class="active" class="nav-link" exact>
              {{ m.title }}
            </NuxtLink>

            <a
              v-else
              :id="'navbarDropdown-' + m.path"
              aria-expanded="false"
              class="nav-link dropdown-toggle"
              data-bs-toggle="dropdown"
              href="#"
              role="button"
            >
              {{ m.title }}
            </a>
            <ul v-if="m.dropdown" :aria-labelledby="'navbarDropdown-' + m.path" class="dropdown-menu">
              <li v-for="item in m.items" :key="item.title">
                <hr v-if="item.divider" class="dropdown-divider">
                <NuxtLink v-else :to="item.path" class="dropdown-item">
                  {{ item.title }}
                </NuxtLink>
              </li>
            </ul>
          </li>
        </ul>
        <ul class="navbar-nav w-100 align-items-center me-auto pb-1 mt-1 mb-lg-0">
          <li class="nav-item me-auto">
            <NuxtLink class="nav-link text-primary h6 mb-0" tag="a" to="/">
              СибГУ им. М.Ф. Решетнева
            </NuxtLink>
          </li>
          <li class="nav-item ms-auto d-lg-flex d-none">
            <form action="/search" class="d-flex" method="GET">
              <input
                aria-label="Search"
                class="form-control me-2 rounded-pill shadow-none"
                placeholder="Найти..."
                type="search"
              >
              <button class="btn rounded-circle position-absolute" type="submit">
                <fa-icon icon="magnifying-glass" transform="shrink-2" />
              </button>
            </form>
          </li>
        </ul>
        <hr class="w-100 my-0 py-0 d-lg-flex d-none">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li v-for="m in menu" :key="m.title" :class="m.dropdown ? 'dropdown' : null" class="nav-item">
            <NuxtLink v-if="!m.dropdown" :to="m.path" active-class="active" class="nav-link" exact>
              {{ m.title }}
            </NuxtLink>

            <a
              v-else
              :id="'navbarDropdown-' + m.path"
              aria-expanded="false"
              class="nav-link dropdown-toggle"
              data-bs-toggle="dropdown"
              href="#"
              role="button"
            >
              {{ m.title }}
            </a>
            <ul v-if="m.dropdown" :aria-labelledby="'navbarDropdown-' + m.path" class="dropdown-menu">
              <li v-for="item in m.items" :key="item.title">
                <hr v-if="item.divider" class="dropdown-divider">
                <NuxtLink v-else :to="item.path" class="dropdown-item">
                  {{ item.title }}
                </NuxtLink>
              </li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'UserMenu',
  data: () => ({
    menu: [
      {
        title: 'Главная',
        dropdown: false,
        path: '/'
      },
      {
        title: 'Университет',
        dropdown: false,
        path: '/university'
      },
      {
        title: 'Образование',
        dropdown: false,
        path: '/learning'
      },
      {
        title: 'Наука и инновации',
        dropdown: false,
        path: '/knowledge'
      },
      {
        title: 'Международное сотрудничество',
        dropdown: false,
        path: '/cooperation'
      },
      {
        title: 'Партнёры',
        dropdown: false,
        path: '/partners'
      }
      // {
      //   title: 'Абитуриентам',
      //   dropdown: true,
      //   items: [
      //     {
      //       title: 'Список поступающих',
      //       path: '/'
      //     },
      //     {
      //       title: 'Задачи института',
      //       path: '/'
      //     },
      //     {
      //       title: 'divider-1',
      //       divider: true
      //     },
      //     {
      //       title: 'Программа 2022',
      //       path: '/'
      //     }
      //   ]
      // },
      // {
      //   title: 'Карта сайта',
      //   dropdown: false,
      //   path: '/map'
      // },
      // {
      //   title: 'Галлерея',
      //   dropdown: false,
      //   path: '/3'
      // },
      // {
      //   title: 'Админ панель',
      //   dropdown: false,
      //   path: '/admin/auth'
      // }
    ],
    second_menu: [
      {
        title: 'Абитуриенту',
        dropdown: false,
        path: '/abiturient'
      },
      {
        title: 'Студенту',
        dropdown: false,
        path: '/student'
      },
      {
        title: 'Выпускнику',
        dropdown: false,
        path: '/graduate'
      },
      {
        title: 'Сотруднику',
        dropdown: false,
        path: '/employee'
      }
    ]
  })
}
</script>
