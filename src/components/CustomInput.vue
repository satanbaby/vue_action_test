<template>
  <div>
    <input type="text" ref="username">
  </div>
</template>

<script lang='ts'>
import Vue from 'vue';
import Component from 'vue-class-component';

@Component
export default class CustomInput extends Vue {
  public $refs!: {
    username: HTMLInputElement,
  };

  public mounted() {
    // Use `input` ref without type cast.
    alert('mounted');
    this.$refs.username.value = '1';
  }
}
</script>

<style>

</style>