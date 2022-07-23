<template>
  <div class="alert alert-primary">
    <h2>title: {{ title }}</h2>
    <p>message: {{ message }}</p>
    <hr />
    <p>Number: {{ num }}</p>
  </div>
</template>

<script>
// リスト4-12 ---------------
export default {
  name: 'HelloWorld',
  props: {
    title: String,
    // num: Number,
    num: {
      type: Number,
      default: 100,
      validator: (value) => {
        console.log(value);
        return value == parseInt(value) && value >= 0 && value <= 100;
      },
    },
  },
  data() {
    return {
      message: 'バリデーション・チェック',
    };
  },
};
</script>
