<template>
  <Modal v-model="chargeModal" class="pages-home-homeIndex-chargeModal" :mask-closable="false"  class-name="vertical-center-modal">
    <p slot="header" style="color:#f60;text-align:center">
      <Icon type="information-circled"></Icon>
      <span>充值中心</span>
    </p>
    <div >
      <Form  :model="formValidate" :label-width="80">
        <Form-item label="用户名：" prop="name" style="margin-bottom: 0">
          artvenny/13800000000
        </Form-item>
        <Form-item label="充值金额：" prop="mail" style="margin-bottom: 0">
          <Row>
            <Col span="22">
            <Input v-model="formValidate.mail" placeholder="请输入邮箱"></Input>
            </Col>
            <Col span="2" style="text-align: center">元</Col>
          </Row>
        </Form-item>
        <Form-item label="支付方式" prop="name" style="margin-bottom: 0">
          支付宝 微信
        </Form-item>
        <Form-item label="支付方式" prop="name" style="margin-bottom: 0">
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
