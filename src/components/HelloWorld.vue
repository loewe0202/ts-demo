<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    name: {{ name }} ···==··· age: {{ age }}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;

  age = 26;
  name = 'hello word!';

  created() {
    this.alertName();
  }

  alertName(): void {
    console.log(this.name + this.msg);
  }
}
</script>

<style scoped lang="scss"></style>
