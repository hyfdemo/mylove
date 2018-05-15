<template>
  <div class="hello">
    <p>致無法韋爾奇</p>
    <a>啟封</a>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}
p{
  width:1rem;
  margin:0 auto;
}
a {
  color: #42b983;
}
</style>
