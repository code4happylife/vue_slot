<template>
  <div class="box2">
    <div class="box3">
      <!-- 通过slot预留一个插槽（占个位置） -->
      <slot name="title"></slot>
    </div>
    <div class="box4">
      <!-- 通过slot预留一个插槽（占个位置） -->
      <slot name="age"></slot>
    </div>
    <slot></slot>
  </div>
</template>

<script></script>

<style>
.box2 {
  width: 300px;
  height: 300px;
  background: #42b983;
}
.box3 {
  width: 300px;
  height: 150px;
  background: #ff007f;
}
.box4 {
  width: 300px;
  height: 50px;
  background: #00ffff;
}
</style>
