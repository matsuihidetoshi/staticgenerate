<template>
  <content-list content-type="articles" title="日記" />
</template>
<script>
import { Component, Vue } from 'nuxt-property-decorator'
import ContentList from '~/components/contents/List.vue'

@Component({
  head () {
    return {
      meta: [
        { hid: 'og:title', property: 'og:title', content: 'og情報がページごとに設定できるかのテスト' },
        { hid: 'og:image', property: 'og:image', content: (process.env.BASE_URL || 'http://localhost:3000') + '/v.png' }
      ]
    }
  },
  components: {
    ContentList
  }
})

export default class Index extends Vue { }
</script>
