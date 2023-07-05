<script>
import Dropdown from './components/dropdown/Dropdown.vue';

export default {
  components: { Dropdown }
}
</script>

<template>
  <div class="center">
    <Dropdown>
      <template v-slot:trigger>
        <button class="btn btn-secondary dropdown-toggle show" type="button" data-bs-toggle="dropdown" aria-expanded="false">
          Dropdown button
        </button>
      </template>
      <template v-slot:menu>
        <li><a class="dropdown-item" href="#">Action</a></li>
        <li><a class="dropdown-item" href="#">Another action</a></li>
        <li><a class="dropdown-item" href="#">Something else here</a></li>
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
