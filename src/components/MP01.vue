<template>
  <div>
    <p>选择所在地区（实名认证主体所在地）</p>
    <van-radio-group v-model="radio" direction="horizontal">
      <van-radio name="1">中国大陆</van-radio>
      <van-radio name="2">中国香港</van-radio>
    </van-radio-group>
    <!-- <slot name="address" :rad='radio'></slot> -->
    <p>手机号码</p>
    <!-- 输入手机号，调起手机号键盘 -->
    <van-field v-model="tel" type="tel" label="+86" placeholder="输入手机号" />
    <van-field v-model="sms" center clearable placeholder="输入验证码">
      <template #button>
        <van-button size="small" type="primary">发送验证码</van-button>
      </template>
    </van-field>
    <!-- 输入密码 -->
    <p>登陆密码</p>
    <van-field v-model="password" type="password" placeholder="输入密码" right-icon="warning-o"/>
    <van-field v-model="password" type="password" placeholder="再次输入密码" right-icon="warning-o"/>
    <p>邀请码（选填）</p>
    <van-field v-model="value" placeholder="输入客户经理邀请码" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      radio: '1',
      tel:'',
      sms:'',
      password: '',
      value:'',
    };
  },
};
</script>

<style></style>
