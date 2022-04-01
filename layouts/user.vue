<template>
  <div>
    <UserMenu />
    <div id="wrapper-page">
      <transition appear name="page">
        <Nuxt />
      </transition>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UserLayout'
}
</script>
