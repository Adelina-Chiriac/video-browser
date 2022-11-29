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

<style>

</style>