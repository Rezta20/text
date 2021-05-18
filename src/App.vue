<template>
  <ul v-for="(list, index) in lists" :key="index">
    <h1>{{ list.title }}</h1>
    <li v-for="(item, index) in list.contents" :key="index">
      {{ item }}
    </li>
  </ul>
</template>

<script>
export default {
  name: "App",
  delimiters: ["${", "}", "."],
  data() {
    return {
      lists: [
        {
          title: "All",
          contents: [
            ".vue",
            "{ { } }",
            "data",
            "v-bind",
            "v-for",
            "computed",
            "v-if",
            "v-show",
            "v-model",
            "v-on",
            "methods",
            "props",
            "typed-props",
            "mounted",
            "axios",
          ],
        },
        {
          title: "First ( first 6 items )",
          contents: [".vue", "{ { } }", "data", "v-bind", "v-for", "computed"],
        },
        {
          title: "Second ( 7th ~)",
          contents: [
            "v-if",
            "v-show",
            "v-model",
            "v-on",
            "methods",
            "props",
            "typed-props",
            "mounted",
          ],
        },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
