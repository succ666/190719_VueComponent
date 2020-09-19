<template>
  <div>
    <h2>Blog列表</h2>
    <ul>
      <Blog v-for="item in blogs" :key="item.id" :blog="item"/>
    </ul>
  </div>
</template>

<script type="text/ecmascript-6">
  import Blog from './Blog'
  export default {
    data() {
      return {
        blogs:[
          {id: 1, title: 'Blog111'},
          {id: 2, title: 'Blog222'},
          {id: 3, title: 'Blog333'},
        ]  
      }
    },
    components:{ // 注册局部组件，只能在当前组件使用
      Blog
    }
  }
</script>
/* scoped: 限定当前组件的样式只对当前组件有效，对外部和内部的其他组件无效 */
<style scoped>
  h2 {
    color: red;
  }
</style>
