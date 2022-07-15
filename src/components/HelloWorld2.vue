<template>
  <div class="alert alert-info">
    <h2>{{ title }}</h2>
    <p>message: {{ message }}</p>
  </div>
</template>
<script>
export default {
  props: {
    title: String,
    message: String,
  },
  // data() {},
};
</script>
