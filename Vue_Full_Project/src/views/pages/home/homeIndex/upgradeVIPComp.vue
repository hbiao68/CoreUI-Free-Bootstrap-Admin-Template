<template>
  <Modal v-model="chargeModal" class="pages-home-homeIndex-chargeModal" :mask-closable="false"  class-name="vertical-center-modal">
    <p slot="header" style="color:#f60;text-align:center">
      <Icon type="information-circled"></Icon>
      <div>升级VIP/续费</div>
      <div>（升级VIP后，可获得后台当前全部功能权限）</div>
    </p>
    <div >
      <Form  :model="formValidate" :label-width="80">
        <Form-item label="用户名：" prop="name" style="margin-bottom: 0">
          artvenny/13800000000
        </Form-item>
        <Form-item label="用户名：" prop="name" style="margin-bottom: 0">
          <Radio-group v-model="phone">
            <Radio label="1">
              <Icon type="social-apple"></Icon>
              <span>1个月（XX元）</span>
            </Radio>
            <Radio label="3">
              <Icon type="social-android"></Icon>
              <span>3个月（XX元）</span>
            </Radio>
            <Radio label="6">
              <Icon type="social-windows"></Icon>
              <span>6个月（XX元）</span>
            </Radio>
            <Radio label="12">
              <Icon type="social-windows"></Icon>
              <span>12个月（XX元）</span>
            </Radio>
          </Radio-group>
        </Form-item>

        <Form-item label="应付金额：" prop="name" style="margin-bottom: 0">
          13800000000 元
        </Form-item>

        <Form-item label="用户名：" prop="name" style="margin-bottom: 0">
          <Radio-group v-model="phone">
            <Radio label="1">
              <Icon type="social-apple"></Icon>
              <span>1个月（XX元）</span>
            </Radio>
            <Radio label="3">
              <Icon type="social-android"></Icon>
              <span>3个月（XX元）</span>
            </Radio>
            <Radio label="6">
              <Icon type="social-windows"></Icon>
              <span>6个月（XX元）</span>
            </Radio>
            <Radio label="12">
              <Icon type="social-windows"></Icon>
              <span>12个月（XX元）</span>
            </Radio>
          </Radio-group>
        </Form-item>

        <Form-item label="支付方式" prop="name" style="margin-bottom: 0">
          <Radio-group v-model="phone">
            <Radio label="1">
              <Icon type="social-apple"></Icon>
              <span>支付宝</span>
            </Radio>
            <Radio label="3">
              <Icon type="social-android"></Icon>
              <span>微信</span>
            </Radio>
          </Radio-group>
        </Form-item>

        <Form-item label="有效期：" prop="name" style="margin-bottom: 0">
          2018年6月20日
        </Form-item>

        <Form-item label="有效期：" prop="name" style="margin-bottom: 0">
          <Checkbox label="twitter">
            <span>勾选默认同意接受《用户协议》</span>
          </Checkbox>
        </Form-item>
      </Form>
    </div>
    <div slot="footer">
      <button class="btn btn-primary" >确认付款</button>
    </div>
  </Modal>
</template>

<script>

  export default {
    name: 'chargeModal',
    data: function () {
      return {
        phone: "",
        userInfoModal: true,
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
