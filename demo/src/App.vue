<template>
  <div id="app">
    <div class="preview" v-html="msg"></div>
    <vue-ueditor-wrap v-model="msg" :config="myConfig"></vue-ueditor-wrap>
  </div>
</template>

<script>
import VueUeditorWrap from '../../src/components/vue-ueditor-wrap'

export default {
  components: {
    VueUeditorWrap
  },
  data () {
    return {
      msg: '',
      myConfig: {
        autoHeightEnabled: true,
        initialFrameWidth: '100%',
        UEDITOR_HOME_URL: '/UEditor/',
      }
    };
  },
};
</script>

<style>
.preview{
  min-height: 200px;
  width: 100%;
}
</style>
