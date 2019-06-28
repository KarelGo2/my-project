<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2>Essential Links</h2>
    <el-button v-on:click="clickHead" class="defaultButton">默认按钮</el-button>
    <el-button @click="clickHead" type="primary">主要按钮</el-button>
    <el-button type="text">文字按钮</el-button>
    <p v-show="msg1">段落</p>
    <p v-text="msg2"> 可以看到啊 </p>

    <ol>
      <li  v-for="(module, index) in modules" :key="index">{{module.msg}}</li>
    </ol>

    <input type="text" v-model="msge">
    <p>{{msge}}</p>
  </div>
</template>
<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: '<h1>你好，世界</h1>',
      className: 'contatiner',
      msg1: false,
      msg2: 'test 2',
      modules: [
        {msg: '第一个'},
        {msg: '第二个'},
        {msg: '第三个'},
        {msg: '第四个'}
      ],
      msge: ''
    }
  },
  methods: {
    clickHead: function () {
      const Name = document.querySelector('.defaultButton')
      console.log(Name)
      alert(this.msg)
    }
  }
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
