<script>
import Index from './Index.vue';

export default {
  components: {
    Index,
  },
};
</script>

<template>
  <div id="app">
    <index />
  </div>
</template>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Noto+Sans+KR:300,400,700&display=swap&subset=korean');

html,
body,
#app {
  margin: 0;
  height: 100%;
  width: 100%;
}

#app {
  display: flex;
  justify-content: center;
  background: linear-gradient(#00AFFF, #0071D1);
}

* {
  font-family: Inter, "Noto Sans KR", sans-serif;
}
</style>
