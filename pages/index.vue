<template>
  <div>
    <section id="index-slider" class="container-fluid">
      <div class="row">
        <div class="col-12 col-slider">
          <div id="carousel" class="carousel slide" data-bs-ride="carousel" data-bs-interval="false">
            <div class="carousel-indicators">
              <button
                type="button"
                data-bs-target="#carousel"
                data-bs-slide-to="0"
                class="active"
                aria-current="true"
                aria-label="Slide 1"
              />
              <button type="button" data-bs-target="#carousel" data-bs-slide-to="1" aria-label="Slide 2" />
            </div>
            <div class="carousel-inner">
              <div v-for="(news, i) in newses" :key="i" class="carousel-item" :class="i === 0 ? 'active' : ''">
                <img :src="news.img" alt="...">
                <div class="carousel-caption">
                  <div class="container">
                    <div class="row justify-content-center">
                      <div class="col-9 col-md-10">
                        <span>{{ news.title }}</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <button class="carousel-control-prev" type="button" data-bs-target="#carousel" data-bs-slide="prev">
              <span class="carousel-control-prev-icon" aria-hidden="true" />
              <span class="visually-hidden">Предыдущий</span>
            </button>
            <button class="carousel-control-next" type="button" data-bs-target="#carousel" data-bs-slide="next">
              <span class="carousel-control-next-icon" aria-hidden="true" />
              <span class="visually-hidden">Следующий</span>
            </button>
          </div>
        </div>
      </div>
    </section>

    <section id="index-news">
      <div class="container">
        <div class="row">
          <div class="col-6 col-sm-auto me-0 me-sm-3">
            <span class="span-link active">Новости</span>
          </div>
          <div class="col-6 col-sm-auto3">
            <span class="span-link">Объявление</span>
          </div>
        </div>
        <div class="row mt-3">
          <div v-for="(news, i) in smallNewses" :key="i" class="col-md-4 col-lg-3 col-6">
            <div class="card bg-transparent border-0 rounded-0">
              <div class="position-relative card-img-wrapper">
                <img :src="news.img" class="card-img-top rounded-0" alt="...">
                <span class="position-absolute px-2 py-1">
                  {{ news.tag }}
                </span>
              </div>
              <div class="card-body px-0">
                <h5 class="card-title">
                  {{ news.title }}
                </h5>
                <p class="card-text">
                  {{ news.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="index-events">
      <div class="container">
        <div class="row">
          <div class="col-6 col-sm-auto me-0 me-sm-3">
            <span class="span-link active">Мероприятия</span>
          </div>
        </div>
        <div class="row gy-2 gy-lg-0 mt-3">
          <div class="col-lg-6 col-12 event big-event">
            <img :src="bigEvent.img" alt="">
            <div class="date">
              <span>{{ bigEvent.date }}</span>
            </div>
            <div class="title">
              {{ bigEvent.title }}
            </div>
          </div>
          <div class="col-lg-6 col-12">
            <div class="row gy-2">
              <div v-for="(event, i) in events" :key="i" class="col-lg-6 col-12 event">
                <img :src="event.img" alt="">
                <div class="date">
                  <span>{{ event.date }}</span>
                </div>
                <div class="title">
                  {{ event.title }}
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout (context) {
    return 'user'
  },
  data: () => ({
    newses: [
      {
        title: 'Апрельское заседание учебного совета',
        img: 'https://spbftu.ru/wp-content/uploads/2022/04/3-2-1-2048x1366.jpg'
      },
      {
        title: 'Победитель грантового конкурса от Росмолодёжи среди вузов',
        img: 'https://spbftu.ru/wp-content/uploads/2022/04/1-1-1.jpg'
      }
    ],
    smallNewses: [
      {
        tag: 'Образование',
        img: 'https://spbftu.ru/wp-content/uploads/2022/04/3-2-1-2048x1366.jpg',
        title: 'Апрельское заседание учебного совета',
        description: 'По традиции собрание началось с торжественной части – вручения наград кафедре физической ...'
      },
      {
        tag: 'Наука',
        img: 'https://spbftu.ru/wp-content/uploads/2022/04/20220412_101916_0000.png',
        title: 'INNOEVENT 2022',
        description: 'С 4 по 8 апреля 2022 года в СибГУ прошла инновационная неделя — важное событие для студентов и компаний...'
      },
      {
        tag: 'Спорт',
        img: 'https://spbftu.ru/wp-content/uploads/2022/04/9vWkcCsQ5KE.jpg',
        title: 'УОЛ СибГУ занял 2 место в спартакиаде',
        description: 'Спартакиада проводилась по 13 видам спорта. УОЛ СибГУ занял почетное 2 место, став...'
      },
      {
        tag: 'Наука',
        img: 'https://spbftu.ru/wp-content/uploads/2022/03/prevyu-9.jpg',
        title: 'Возглавили команду экспертов для научной работы о насекомых',
        description: 'В ходе работы были проанализированы основные насекомые-инвайдеры...'
      }
    ],
    bigEvent: {
      date: 'Пятница, 22 апреля',
      img: 'https://sibsau.ru/files/17471/',
      title: 'ПРЕДСТАВЛЕНИЕ НОВОГО САЙТА УОЛ СИБГУ'
    },
    events: [
      {
        date: 'Среда, 20 апреля',
        img: 'https://medvestnik.ru/apps/mv/assets/cache/files/content/news/736/73699/front-jpg/front-z-400.jpg?time=1476602743',
        title: 'НАУЧНО-МЕТОДИЧЕСКИЙ СОВЕТ'
      },
      {
        date: 'Суббота, 16 апреля',
        img: 'https://www.volgatech.net/upload/iblock/c56/c5656f3977b8f24c4b1e5552adaa8386.jpg',
        title: 'УЧЕБНО-ОПЫТНЫЙ ЛЕСХОЗ ПГТУ ГОТОВИТСЯ К ПОЖАРООПАСНОМУ СЕЗОНУ'
      },
      {
        date: 'Пятница, 15 апреля',
        img: 'https://tatarstan.ru/file/news/221_n1593029_big.jpg',
        title: 'МАСТЕР КЛАСС ПО ИЗУЧЕНИЮ РАСТЕНИЙ'
      },
      {
        date: 'Пятница, 8 апреля',
        img: 'https://rsmu.ru/fileadmin/templates/img/news/2021/US_18_10_2021.jpg',
        title: 'ЗАСЕДАНИЕ УЧЕБНОГО СОВЕТА'
      }
    ]
  }),
  mounted () {
    this.$nextTick(() => {
      setTimeout(() => {
        this.resizeEvent()
      }, 1000)

      window.addEventListener('resize', () => {
        this.resizeEvent()
      })
    })
  },
  methods: {
    resizeEvent () {
      const events = document.getElementsByClassName('event')
      for (let i = 0; i < events.length; i++) {
        const event = events.item(i)
        event.style.height = event.offsetWidth - 8 + 'px'
      }
    }
  }
}
</script>
