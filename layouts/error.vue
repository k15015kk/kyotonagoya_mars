<template>
  <v-app dark>
    <div class="pa-4">
      <h2 v-if="error.statusCode === 404">{{ pageNotFound }}</h2>
      <h2 v-else>{{ otherError }}</h2>
      <div v-if="error.statusCode === 404">
        ページが見つかりませんでした．
        <div class="pt-4">
          <h3>もしかしたら？</h3>
          <ul>
            <li>リンクが間違っている</li>
          </ul>
        </div>

        <div class="pt-4">
          <h3>以下の要因が考えられます</h3>
          <ul>
            <li>公開期限が過ぎておりリンク先が切れている</li>
            <li>本当にページが存在しない</li>
          </ul>
        </div>
      </div>
    </div>
    <NuxtLink class="pa-4" to="/">TopPage</NuxtLink>
  </v-app>
</template>

<script>
module.exports = {
  layout: 'empty',
  props: {
    error: {
      type: Object,
      default: null,
    },
  },
  data() {
    return {
      pageNotFound: '404 Not Found',
      otherError: 'An error occurred',
    }
  },
  head() {
    const title =
      this.error.statusCode === 404 ? this.pageNotFound : this.otherError
    return {
      title,
    }
  },
}
</script>

<style scoped>
h1 {
  font-size: 20px;
}
</style>
