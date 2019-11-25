<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>{{count}}</h2>
    <Button type="default" @click="addCount">点击加一</Button>
  </div>
</template>

<script lang="ts">
import { Component,Vue,Prop} from "vue-property-decorator";
import {Button} from "element-ui";


// 装饰器
@Component({
  components: {
    Button
  }
})
export default class HelloWorld extends Vue {
  data(){
    return {
      
    }
  };
  // 组件传至通过@Prop
  @Prop() private msg!: string;
  // 公有属性:vuex
  public count:number = this.$store.state.count;
  // 方法
  addCount():void{ //void没有返回值
    this.count ++
  }
}
</script>

<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
</style>
