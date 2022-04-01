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
              <button type="button" data-bs-target="#carousel" data-bs-slide-to="2" aria-label="Slide 3" />
            </div>
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img src="http://placehold.jp/1920x1080.png" class="d-block img-fluid w-100" alt="...">
                <div class="carousel-caption">
                  <div class="container">
                    <div class="row justify-content-center">
                      <div class="col-9 col-md-10">
                        <span>Университет Решетнёва начинает сотрудничать с Казанским «ИТ-парком»</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="carousel-item">
                <img src="http://placehold.jp/1920x1080.png" class="d-block w-100" alt="...">
                <div class="carousel-caption">
                  <div class="container">
                    <div class="row justify-content-center">
                      <div class="col-9 col-md-10">
                        <span>Университет Решетнёва начинает сотрудничать с Казанским «ИТ-парком»</span>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="carousel-item">
                <img src="http://placehold.jp/1920x1000.png" class="d-block w-100" alt="...">
                <div class="carousel-caption">
                  <div class="container">
                    <div class="row justify-content-center">
                      <div class="col-9 col-md-10">
                        <span>Университет Решетнёва начинает сотрудничать с Казанским «ИТ-парком»</span>
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
          <div v-for="i in 4" :key="i" class="col-md-4 col-lg-3 col-6">
            <div class="card bg-transparent border-0 rounded-0">
              <div class="position-relative card-img-wrapper">
                <img src="http://placehold.jp/300x300.png" class="card-img-top rounded-0" alt="...">
                <span class="position-absolute px-2 py-1">
                  Наука
                </span>
              </div>
              <div class="card-body px-0">
                <h5 class="card-title">
                  Заголовок карточки
                </h5>
                <p class="card-text">
                  Небольшой пример текста, который должен основываться на названии карточки и составлять основную часть содержимого карты.
                </p>
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
  }
}
</script>
