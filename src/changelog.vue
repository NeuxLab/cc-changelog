<template>
  <div class="changelog ui card cc-item">
    <div class="cc-item-header content">
      <div class="header">1.0.5 更新日志</div>
    </div>
    <div class="cc-item-content content cc-content">
      <div class="cc-text">
        <dl>
          <dd>发布入门操作视频，请点击前往<a href='https://ccyixia.com' target="_blank">官网</a>查看</dd>
          <dd>为通知窗口增加右键菜单，包含 <code>置顶</code> <code>Pin</code> 等功能</dd>
          <dd>修复自动更新没有默认开启的 bug </dd>
          <dd>调整样式 & 修复其他 bug</dd>
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
