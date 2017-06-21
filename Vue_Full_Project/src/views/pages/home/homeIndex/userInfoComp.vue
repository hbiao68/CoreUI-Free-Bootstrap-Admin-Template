<template>
  <Modal v-model="userInfoModal" class="pages-home-homeIndex-chargeModal" :mask-closable="false"  class-name="vertical-center-modal">
    <p slot="header" style="color:#f60;text-align:center">
      <Icon type="information-circled"></Icon>
      <span>用户信息</span>
    </p>
    <div >
      <Row>
        <Col span="12">
          <div class="row_item">
            <div class="float_left width_100px">用户名：</div>
            <div class="margin_left_100">artvenny/138****1234</div>
          </div>
        </Col>

        <Col span="12">
          <div class="row_item">
            <div class="float_left width_100px">易撰ID：</div>
            <div class="margin_left_100">0000001</div>
          </div>
        </Col>

        <Col span="12">
          <div class="row_item">
            <div class="float_left width_100px">账号状态：</div>
            <div class="margin_left_100">试用账号/VIP</div>
          </div>
        </Col>

        <Col span="12">
          <div class="row_item">
            <div class="float_left width_100px">到期时间：</div>
            <div class="margin_left_100">2018年6月20日15:32:56</div>
          </div>
        </Col>

        <Col span="12">
        <div class="row_item">
          <div class="float_left width_100px">我的易豆：</div>
          <div class="margin_left_100">0000001</div>
        </div>
        </Col>
        <Col span="12">
        <div class="row_item">
          <div class="float_left width_100px">消费记录：</div>
          <div class="margin_left_100">
            <button class="btn btn-primary" >查看</button>
          </div>
        </div>
        </Col>
        <Col span="12">
        <div class="row_item">
          <div class="float_left width_100px">系统消息：</div>
          <div class="margin_left_100">
            <Icon type="chatboxes"></Icon>
          </div>
        </div>
        </Col>
        <Col span="12">
        <div class="row_item">
          <div class="float_left width_100px">充值：</div>
          <div class="margin_left_100">0000001</div>
        </div>
        </Col>
      </Row>
    </div>
    <div slot="footer">
    </div>
  </Modal>
</template>

<script>

  export default {
    name: 'chargeModal',
    data: function () {
      return {
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
