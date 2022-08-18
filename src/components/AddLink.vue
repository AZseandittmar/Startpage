<template>
  <label for="link">
  <input type="text" id="link" name="link" v-model="link">

</template>

<script>
export default {
  name: "AddLink",
  data() {
    return {
      link: '',
      name: '',
      desc: '',
      datetime: ''
    }
  }
}
</script>

<style></style>