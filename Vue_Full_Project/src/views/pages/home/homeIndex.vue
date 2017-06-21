<template>
  <div class="pages-home-index">
    <div>
      <!-- 账号信息 -->
      <div class="float_left width_50">
        <div>账号信息</div>
        <div class="row_item">
          <div class="float_left width_100px">用户名称</div>
          <div class="margin_left_100">artvenny（微信号）</div>
        </div>

        <div class="row_item">
          <div class="float_left width_100px">易撰ID：</div>
          <div class="margin_left_100">0000001</div>
        </div>

        <div class="row_item">
          <div class="float_left width_100px">账号状态：</div>
          <div class="margin_left_100">
            <span>试用版/VIP</span>
            <span><button class="btn btn-primary">升级VIP/续费</button></span>
          </div>
        </div>

        <div class="row_item">
          <div class="float_left width_100px">到期时间：</div>
          <div class="margin_left_100">2017/09/12  19:24:58</div>
        </div>
      </div>

      <!-- 资金管理 -->
      <div class="float_left width_50">
        <div>资金管理</div>
        <div class="row_item">
          <div class="float_left width_100px">易豆：</div>
          <div class="margin_left_100">
            <span>试用版/VIP</span>
            <span><button class="btn btn-primary" @click="showChargeModal">充值</button></span>
         </div>
        </div>
        <div class="row_item">
          <div class="float_left width_100px">消费记录：</div>
          <div class="margin_left_100">
            <span>￥7848484</span>
            <span><button class="btn btn-primary">查看</button></span>
          </div>
        </div>
      </div>

      <div class="clear_both"></div>
    </div>

    <!-- 安全中心 -->

    <safety-comp></safety-comp>

    <!-- banner -->
    <swiper-comp></swiper-comp>

    <!-- 新闻 -->
    <msg-record-comp></msg-record-comp>

    <component :is="modalType"></component>
  </div>
</template>

<script>

  import chargeModal from './homeIndex/chargeModal.vue'
  import resetPwdModal from './homeIndex/resetPwdModal.vue'
  import swiperComp from './homeIndex/swiperComp.vue'
  import msgRecordComp from './homeIndex/msgRecordComp.vue'
  import safetyComp from './homeIndex/safetyComp.vue'
  import forgetPwdModal from './homeIndex/forgetPwdModal.vue'
  import userInfoComp from './homeIndex/userInfoComp.vue'
  import upgradeVIPComp from './homeIndex/upgradeVIPComp.vue'

  export default {
    name: 'Login',
    data: function () {
      return {
        // 模态框的类型
        modalType: ""
      }
    },
    methods: {
      loginAction: function () {
        this.$router.push({name: 'Dashboard'})
      },
      //显示充值模态框
      showChargeModal: function () {
          this.modalType = "chargeModal";
      }
    },
    components: {
      upgradeVIPComp,
      userInfoComp,
      forgetPwdModal,
      safetyComp,
      resetPwdModal,
      msgRecordComp,
      swiperComp,
      chargeModal
    }
  }
</script>

<style scoped lang="scss">
  .pages-home-index{

    .ivu-card:hover {
       box-shadow: none;
    }
  }
</style>
