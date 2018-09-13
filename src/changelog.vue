<template>
  <div class="changelog ui card cc-item">
    <div class="cc-item-header content">
      <div class="header">1.1.1 更新日志</div>
    </div>
    <div class="cc-item-content content cc-content">
      <div class="cc-text">
        <dl>
          <dd>增加修改本地数据目录的选项</dd>
          <dd>修复 Word 和 Excel 的误触发问题</dd>
          <dd>忽略来自常见密码管理软件的内容</dd>
          <dd>增加开启测试版更新的选项</dd>
          <dd>修复其他 bug</dd>
        </dl>
      </div>
    </div>
    <div class="cc-item-footer content extra">
      <button class='btn btn-primary btn-revert' @click='dismiss'>知道了</button>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    dismiss() {
      this.$emit("dismiss")
    }
  },
  mounted(){
    
  }
}
</script>


<style lang="less">
.changelog.cc-item {
  background: #4d7ed8;
  color: white;

  .btn-revert {
    border-color: white;
  }
  dd {
    line-height: 1.2;
  }

  a {
    color: white;
    text-decoration: underline;
    cursor: pointer;
  }
}
</style>
