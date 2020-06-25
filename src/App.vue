<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <editor v-model="text" 
        api-key="qagffr3pkuv17a8on1afax661irst1hbr4e6tbv888sz91jc"
       :init="{
         height: 500,
         plugins: [
           'advlist autolink lists link image charmap print preview anchor',
           'searchreplace visualblocks code fullscreen',
           'insertdatetime media table paste code help wordcount'
         ],
         toolbar:
           'undo redo | formatselect | bold italic backcolor | \
           alignleft aligncenter alignright alignjustify | \
           bullist numlist outdent indent | removeformat | help |\
           table tabledelete | tableprops tablerowprops tablecellprops | tableinsertrowbefore tableinsertrowafter tabledeleterow | tableinsertcolbefore tableinsertcolafter tabledeletecol',
       }"></editor>
  </div>
</template>

<script>
import Editor from '@tinymce/tinymce-vue';
export default {
  name: 'App',
  data() {
    return {
      text: ''
    }
  },
  components: {
    'editor': Editor // <- Important part
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
