<script setup>
import { useRouter, useRoute} from 'vue-router'

const router = useRouter()
const route = useRoute();

console.log(router)
console.log(route)
</script>

<template>
  <div class="about">
    <h1>This is an about page </h1>
    <!-- テンプレート内では this なしで、$router や $route にアクセス-->
    <p>{{ $router.options.routes[0].name}}</p> <!-- home と出力-->
    <p>{{ $route.path}}</p> <!-- /about と出力 -->
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
