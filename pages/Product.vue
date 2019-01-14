<template>
  <h2>{{ title }}</h2>
</template>

<script>
export default {
  async asyncData (context) {
    return await new Promise(resolve => {
      setTimeout(() => {
        resolve({
          title: `このページはNuxt社のプロダクト情報のページです。(${ context.isServer ? 'サーバーサイドレンダリング' : 'クライアントサイドレンダリング' })`
        })
      }, 1000)
    })
  }
}
</script>
