<script>
import Dropdown from './components/dropdown/Dropdown.vue';

export default {
  components: { Dropdown }
}
</script>

<template>
  <div class="center">
    <Dropdown>
      <template v-slot:trigger="{ toggleClass, toggle }">
        <button class="btn btn-secondary dropdown-toggle" :class="toggleClass" @click="toggle" type="button" data-bs-toggle="dropdown" aria-expanded="false">
          Dropdown button
        </button>
      </template>
      <template v-slot:menu="{ toggle }">
        <li><a class="dropdown-item" href="#" @click.prevent="toggle">Action</a></li>
        <li><a class="dropdown-item" href="#" @click.prevent="toggle">Another action</a></li>
        <li><a class="dropdown-item" href="#" @click.prevent="toggle">Something else here</a></li>
      </template>
    </Dropdown>
  </div>
</template>

<style scoped>
.center {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
}
</style>
