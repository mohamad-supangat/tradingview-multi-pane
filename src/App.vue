<script setup lang="ts">
import { ref } from "vue";
const chartUrl =
  "https://www.tradingview.com/chart/oR6qgXja/?symbol=BINANCE%3ABNBBUSDPERP";

const filter = {
  urls: [
    "https://*.tradingview.com/static/bundles/trial-notification.*.js",
    "https://securepubads.g.doubleclick.net/gampad/ads?*",
  ],
};

// const webviewRefs = ref([]);

// setTimeout(() => {
//   console.log(webviewRefs.value[1]);
// }, 1000);
</script>
<template>
  <webview
    v-for="i in 4"
    :src="chartUrl"
    class="bg-primary"
  ></webview>
</template>
<style lang="scss">
// using http://jsfiddle.net/ZGMwG/
* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html,
body {
  height: 100%;
  width: 100%;
}

webview {
  width: 50%;
  height: 50vh;
  float: left;
}

webview:nth-of-type(1) {
  background: #ccc;
}

webview:nth-of-type(2) {
  background: #bbb;
  border-left: 1px solid #f00;
}

webview:nth-of-type(3) {
  background: #aaa;
  border-top: 1px solid #f00;
}

webview:nth-of-type(4) {
  background: #ddd;
  border-top: 1px solid #f00;
  border-left: 1px solid #f00;
}
</style>
