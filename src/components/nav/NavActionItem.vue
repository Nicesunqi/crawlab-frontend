<template>
  <div class="nav-action-item">
    <slot></slot>
  </div>
</template>

<script lang="ts">
import {defineComponent} from 'vue';

export default defineComponent({
  name: 'NavActionItem',
  setup() {
    return {};
  },
});
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";

.nav-action-item {
  margin: 10px 0;
  height: auto;
  display: flex;
  align-items: center;
  color: $navActionsItemColor;

  & + .nav-action-item {
    margin-left: 10px;
  }
}
</style>
<style scoped>
.nav-action-item >>> .title {
  color: inherit;
}

.nav-action-item >>> .label {
  color: inherit;
  font-size: 14px;
  margin-right: 5px;
  margin-left: 5px;
}

.nav-action-item >>> .el-button.el-button--small {
  height: 32px;
}

.nav-action-item >>> .el-button:not(.is-circle) .fa {
  margin-right: 0;
}

.nav-action-item >>> .el-button .icon + span {
  margin-left: 5px;
}
</style>
