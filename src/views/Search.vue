<template>
  <div class="wrapper">
    <Claim />
    <SearchInput />

  </div>
</template>

<script>
  import axios from 'axios';
  import debounce from 'lodash.debounce';
  const API = 'https://images-api.nasa.gov/search';
  import Claim from '../components/Claim.vue';
  import SearchInput from '../components/SearchInput.vue';
export default {
  name: 'Search',
  components: {
    Claim,
    SearchInput,
  },
  data() {
    return {
      searchValue: '',
      results: [],
    };
  },
  methods: {
    handleInput: debounce(function() {
      axios.get(`${API}?q=${this.searchValue}&media_type=image`)
        .then((response) => {
          this.results = response.data.collection.items;
        })
        .catch((error) => {
          console.log(error);
        });
    }, 500),
  },
};
</script>

<style lang="scss" scoped>
  .wrapper {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0;
    padding: 30px;
    width:100%;
    justify-content: center;
    align-items: center;
    background-image: url('../assets/heroimage.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 80% 0%;

  }


</style>
