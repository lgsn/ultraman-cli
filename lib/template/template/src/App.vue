<template>
<%_ if (rootOptions.vueVersion === '3') { _%>
  <h1>Vue3</h1>
<%_ } else { _%>
  <div id="app">
    <p>AOTE</p>
  </div>
<%_ } _%>
</template>
<%_ if (!rootOptions.bare) { _%>

<script>

export default {
  name: 'App'
}
</script>

<%_ if (rootOptions.cssPreprocessor !== 'stylus') { _%>
<style<%-
  rootOptions.cssPreprocessor
    ? ` lang="${
        rootOptions.cssPreprocessor.includes('sass')
          ? 'scss'
          : rootOptions.cssPreprocessor
      }"`
    : ``
%>>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
<%_ } else { _%>
<style lang="stylus">
#app
  font-family Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
  margin-top 60px
</style>
<%_ } _%>
<%_ } _%>
