<template>
  <div id="app" class="app">
    <div class="oppsite">反面的内容</div>
    <div class="front">正面的内容</div>
  </div>
</template>

<script>

export default {
  name: 'app'
}
</script>

<style>
.app{
  width:200px;
  height:200px;
  margin:20px auto;
  position:relative;
}
.front,.oppsite{
  position:absolute;
  left:0;
  top:0;
  right:0;
  bottom:0;
  background-color:blue;
  transition:all 2s ease-in-out;
  backface-visibility:hidden;
}
.oppsite{
  transform:rotateY(180deg);
  -ms-transform:rotateY(180deg);
  -moz-transform:rotateY(180deg);
  -webkit-transform:rotateY(180deg);
  -o-transform:rotateY(180deg);
}
.front{
  background-color:red;
}

.app:hover .front{
  transform:rotateY(180deg);
  -ms-transform:rotateY(180deg);
  -moz-transform:rotateY(180deg);
  -webkit-transform:rotateY(180deg);
  -o-transform:rotateY(180deg);
}
.app:hover .oppsite{
  transform:rotateY(0deg);
  -ms-transform:rotateY(0deg);
  -moz-transform:rotateY(0deg);
  -webkit-transform:rotateY(0deg);
  -o-transform:rotateY(0deg);
}
</style>
