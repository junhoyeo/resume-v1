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
@import url('https://fonts.googleapis.com/css?family=Noto+Sans+KR:300,400,700,900&display=swap&subset=korean');

html,
body,
#app {
  margin: 0;
  width: 100%;
}

html {
  // background: linear-gradient(#00AFFF, #0071D1);
  // background-repeat: no-repeat;
}

#app {
  display: flex;
  justify-content: center;
}

* {
  font-family: Inter, "Noto Sans KR", sans-serif;
}
</style>
