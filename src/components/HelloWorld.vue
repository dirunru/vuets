<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";

// 装饰器
@Component
export default class HelloWorld extends Vue {
  // 组件传至通过@Prop
  @Prop() private msg!: string;
}
</script>

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
</style>
