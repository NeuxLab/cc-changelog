<template>
  <div class="changelog ui card cc-item">
    <div class="cc-item-header content">
      <div class="header">1.0.3 更新日志</div>
    </div>
    <div class="cc-item-content content cc-content">
      <div class="cc-text">
        <dl>
          <dd>通知窗口增加置顶功能，快捷键 <kbd>空格</kbd>
          </dd>
          <dd>通知窗口增加 Pin 功能，方便快速标记，快捷键 <kbd>!</kbd>
          </dd>
          <dd>列表页面可以对条目按 <kbd>空格</kbd> 进行查看编辑</dd>
          <dd>修复与其他粘贴工具的冲突问题 </dd>
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

}
</style>
