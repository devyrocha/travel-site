<template>
  <div>
    <input class="inputSearch" type="text" placeholder="Buscar por cidade" />
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.inputSearch {
  position: absolute;
  top: 4rem;
  left: 4rem;
  padding: 15px;
  width: 30%;
  font-size: 18px;
  outline: none;
  border: none;
  border-radius: 10px;
  font-weight: 300;
}
</style>