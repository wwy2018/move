<template>
  <div class="hello">
    <div><button class="b-round" @click="move">点我开si</button></div>
    <div :class="['img-holder',isactive? 'active': '']"><img src="../assets/logo.png" alt="" class="img-1"></div>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      a: 100,
      isactive: false
    }
  },
  created () {
    console.log(window.orientation)
  },
  methods: {
    move(){
      this.isactive? this.isactive=false : this.isactive=true
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  background: green;
  height: 1000px;
}
.b-round{
  border-radius: 50%;
  background: #ffffff;
  border: 1px solid #666;
  width: 50px;
  height: 50px;
  padding: 10px;
}
.img-holder{
  /* position: relative; */
}
.img-1{
  width: 50px;
  height: 50px;
}
.active{
  animation: m1 2s forwards;
}
@keyframes m1 {
  from{
    transform: translateY(0)
  }
  to{
    transform: translateY(100px)
  }
}
</style>
