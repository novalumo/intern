# WordPress REST API

## 記事の取得

`/wp-json/wp/v2/posts/`で記事一覧を取得でき、`/wp-json/wp/v2/posts/投稿id`で指定したIDの記事データを取得できる。
なお、返ってくる主なデータは以下の通り。

### id
記事のID

### date
記事の投稿時間

### date_gmt
記事の投稿時間（GMT表記）

### guid
記事のURL（ID表示）

### modified
記事の編集日時

### modified_gmt
記事の編集日時（GMT表記）

### slug
記事のパーマリンク

### status
記事の公開状態
publish（公開）, future（公開予約）, draft（下書き）, pending（非公開）, private（限定公開）のいずれかが得られます。

### type
投稿の種類。記事であれば「post」

### link
記事のURL

### title
記事のタイトル

### content
記事本文

### excerpt
記事の引用時に表示されるテキスト

### author
投稿者

### featured_media
アイキャッチ画像のID

### comment_status
コメントの状態
open(受け付ける)、closed(受け付けない)のうちどちらか

### ping_status
トラックバックを受け付けるかどうか
open(受け付ける)、closed(受け付けない)のうちどちらか

### sticky
公開状態の「この投稿を先頭に固定表示」にあたるパラメータ
True, Falseのbool値

### template
記事のテンプレート

### format
記事のフォーマット
standard, aside, chat, gallery, link, image, quote, status, video, audioのいずれか。
一般的な記事であれば「standard」

### meta
記事のメタ情報

### categories
記事のカテゴリー（slugではなくカテゴリーに対応するID）

### tags
記事のタグ

## 使用例

### Nuxt.js + Axios

```vue
<template>
  <div>
    <span>{{ posts }}</span>
  </div>
</template>

<script>
export default {
  data() {
    return {
      posts: null
    }
  },
  methods: {
    async fetchPosts() {
      this.posts = await this.$axios.$get('http://localhost:8888/wordpress_test/wp-json/wp/v2/posts/')
    }
  },
  mounted() {
    this.fetchPosts()
  }
}
</script>
```
