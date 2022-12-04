<template>
  <div>
    <input @input="onInput" />
  </div>
</template>

<script>
export default {
  name: "SearchBar",
  methods: {
    onInput: function(event) {
      this.$emit("searchTermChange", event.target.value);
    }
  }
};
</script>

<style scoped>
  input {
    width: 75%;
    height: 35px;
  }

  div {
    margin: 20px;
    text-align: center;
  }
</style>