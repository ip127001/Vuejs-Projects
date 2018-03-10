<template>
  <div class="row">
    <div class="col-sm-6 col-md-3">
      <div class="box">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
}
</script>

<style>
.box {
  padding: 10px;
  border: 1px solid lightseagreen;
  box shadow: 0px 3px 3px 0px rgba(0, 0, 0, .19);
}
</style>
