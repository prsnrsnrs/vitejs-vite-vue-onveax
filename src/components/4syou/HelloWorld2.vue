<script>
import { h } from 'vue';

export default {
  name: 'HelloWorld',
  data() {
    return {
      title: 'HelloWorld',
      message: 'This is sample message.',
    };
  },
  render() {
    // return `title: {{ title }} mess: {{ message }}`;

    // リスト4-4 JSXあたり
    return h(
      'div',
      {
        class: '',
      },
      [h('h2', this.title), h('p', this.message)]
    );
  },
};
</script>
