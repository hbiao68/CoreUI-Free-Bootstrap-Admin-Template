<template>
  <Modal v-model="chargeModal" class="pages-home-homeIndex-chargeModal" :mask-closable="false"  class-name="vertical-center-modal">
    <p slot="header" style="color:#f60;text-align:center">
      <Icon type="information-circled"></Icon>
      <span>修改密码</span>
    </p>
    <div >
      <Form  :model="formValidate" :label-width="80">
        <Form-item label="手机号码：" prop="mail" style="margin-bottom: 0">
          <Row>
            <Col span="22">
            <Input v-model="formValidate.mail" placeholder="手机号码"></Input>
            </Col>
          </Row>
        </Form-item>

        <Form-item label="旧密码：" prop="mail" style="margin-bottom: 0">
          <Row>
            <Col span="8">
            <Input v-model="formValidate.mail" placeholder="旧密码"></Input>
            </Col>
            <Col span="8">
              <button class="btn btn-primary" >获取验证码</button>
            </Col>
          </Row>
        </Form-item>

        <Form-item label="输入新密码：" prop="mail" style="margin-bottom: 0">
          <Row>
            <Col span="22">
            <Input v-model="formValidate.mail" placeholder="输入新密码"></Input>
            </Col>
          </Row>
        </Form-item>

        <Form-item label="再输入一次：" prop="mail" style="margin-bottom: 0">
          <Row>
            <Col span="22">
            <Input v-model="formValidate.mail" placeholder="再输入一次"></Input>
            </Col>
          </Row>
        </Form-item>
      </Form>
    </div>
    <div slot="footer">
      <button class="btn btn-primary" >确认提交</button>
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
