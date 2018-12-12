<template>
  <div class="searchWrapper">
      <input
        name="search"
        id="search"
        v-model="searchValue"
        @input="handleInput"
      />
  </div>
</template>

<script>
  export default {
    name: 'SearchInput.vue',
  };
</script>

<style lang="scss" scoped>
  .searchWrapper {
    margin-top: 50px;
    display: flex;
    flex-direction: column;
    width: 260px;
  }

  .search {
    width: 250px;
    display: flex;
    flex-direction: column;
  }

    input {
      height: 30px;
      border: 0;
      border-bottom: 1px solid black;
      background: none;
    }
</style>
