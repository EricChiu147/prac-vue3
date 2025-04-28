<template>
  <p>
    Hello World<br>
  </p>
  <p v-if="x === 0">
    x = 0
  </p>
  <p v v-else-if="x === 1">
    x = 1
  </p>
  <p v-else>
    x out of range
  </p>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isShow: true,
      x: 0,
    };
  },
};
</script>
