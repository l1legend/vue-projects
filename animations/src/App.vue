<template>
<button type="button" @click="flag = !flag">Toggle</button>

<!-- <transition name="fade" mode="out-in">
<h2 v-if="flag" key="main">Hello world!</h2>
<h2 v-else key="secondary">Another hello!</h2>
</transition> -->

<transition name="zoom">
<h2 v-if="flag">Hello</h2>
</transition>

</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      flag: false,
    };
  },
};
</script>

<style>
h2 {
  width: 400px;
  padding: 20px;
  margin: 20px;
}

.fade-enter-from {
  opacity: 0;
}

.fade-enter-active {
  transition: all .75s linear;
}

.fade-leave-to {
  transition: all .75s linear;
  opacity: 0;
}
</style>
