<template>
  <div>
    <div>小二：首页  state.count: {{ count }} </div>
    <router-link to="/detail">detail</router-link>
    <br />
    <router-link to="/list">list</router-link>
    <br />
    <el-button type="primary" @click="handleClick">子应用间跳转</el-button>
    <el-alert
      title="这是一个 Element 的组件"
      type="success"
    >
    </el-alert>
  </div>
</template>

<script>
import { mapGetters } from 'vuex';
export default {
  computed: {
    ...mapGetters(['count'])
  },
  methods: {
    handleClick: () => {
      window.history.pushState({}, '', '/dashboard');
    }
  }
}
</script>>