<template>
  <div class="page page-with-padding">
    <wv-button type="default" @click="showSuccess">成功提示</wv-button>
    <wv-button type="default" @click="showError">出错提示</wv-button>
    <wv-button type="default" @click="showText">纯文本提示</wv-button>
    <wv-button type="default" @click="showLoading">加载提示</wv-button>
  </div>
</template>

<script>
export default {
  methods: {
    showSuccess () {
      this.$toast.success('操作成功')
    },

    showError () {
      this.$toast.fail({
        duration: 1000,
        message: '操作失败'
      })
    },

    showText () {
      this.$toast.text({
        duration: 1000,
        message: 'hello'
      })
    },

    showLoading () {
      this.$toast.loading({
        message: 'Loaidng',
        duration: 500000
      })
    }
  }
}
</script>
