<template>
  <div style="padding:30px;">
    <el-alert :closable="false" :title="key" type="success" />
      <router-view :key="key" />
    </el-alert>
  </div>
</template>
<script>
export default {
  computed: {
    key() {
      return this.$route.name !== undefined ? this.$route.name + ' ' + +new Date() : this.$route + ' ' + +new Date()
    }
  }
}
</script>
