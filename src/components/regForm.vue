<template>
	<div class="login-form">
    <div class="g-form">
      <div class="g-form-line" v-for="formLine in formData">
        <span class="g-form-label">{{ formLine.label }}：</span>
        <div class="g-form-input">
          <input type="text" 
           placeholder="请输入用户名">
        </div>
      </div>
      <div class="g-form-line">
        <div class="g-form-btn">
          <a class="button">登录</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default{
	data () {
    return {
      formData:[{label:'用户名'},{label:'密码'}]
    }
  }
}
</script>

<style scoped>
.dialog-wrap {
  position: fixed;
  width: 100%;
  height: 100%;
}
.dialog-cover {
  background: #000;
  opacity: .3;
  position: fixed;
  z-index: 5;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
.dialog-content {
  width: 50%;
  position: fixed;
  max-height: 50%;
  overflow: auto;
  background: #fff;
  top: 20%;
  left: 50%;
  margin-left: -25%;
  z-index: 10;
  border: 2px solid #464068;
  padding: 2%;
  line-height: 1.6;
}
.dialog-close {
  position: absolute;
  right: 5px;
  top: 5px;
  width: 20px;
  height: 20px;
  text-align: center;
  cursor: pointer;
}
.dialog-close:hover {
  color: #4fc08d;
}
</style>