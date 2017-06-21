<template>
  <div>
    <div>安全中心1</div>
    <div class="row_item">
      <div class="float_left width_100px">绑定手机：</div>
      <div class="margin_left_100">
        <div class="float_right width_100px">
          <button class="btn btn-primary">设置/修改</button>
        </div>
        <div class="margin_right_100">
          可用于登录、密码找回等安全保护/138****1234
        </div>
      </div>
    </div>

    <div class="row_item">
      <div class="float_left width_100px">密码修改：</div>
      <div class="margin_left_100">
        <div class="float_right width_100px">
          <button class="btn btn-primary">设置修改</button>
        </div>
        <div class="margin_right_100">
          设置密码前，请先绑定手机
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'chargeModal',
    data: function () {
      return {
        chargeModal: true,
        formValidate: {}
      }
    },
    methods: {
    },
    components: {
    }
  }
</script>

<style scoped lang="scss">
  .pages-home-homeIndex-chargeModal{
  }
</style>
