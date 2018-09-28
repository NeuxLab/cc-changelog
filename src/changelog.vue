<template>
  <div class="changelog ui card cc-item">
    <div class="cc-item-header content">
      <div class="header">{{ version }} 更新日志</div>
    </div>
    <div class="cc-item-content content cc-content">
      <div class="cc-text">
        <dl>
          <dd>增加 <kbd>多选</kbd> 功能，可以对多个项目进行删除</dd>
          <dd>增加 <kbd>合并</kbd> 功能，多选之后可以合并文本或文件类型</dd>
          <dd>增加 <kbd>文本编辑</kbd> 功能，可以对文本项目进行修改</dd>
          <dd>修正托盘图标的 <kbd>关于</kbd> 功能</dd>
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
  computed: {
    version() {
      return cc.getVersion()
    }
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
