<template>
  <div class="home-page">
    <McvBanner />
    <div class="container page">
      <div class="row">
        <div class="col-md-9">
          <McvFeedToggler />
          <McvMainFeed :api-url="apiUrl" />
        </div>
        <McvPopularTags />
      </div>
    </div>
  </div>
</template>

<script>
import McvMainFeed from '@/components/MainFeed'
import McvPopularTags from '@/components/PopularTags'
import McvBanner from '@/components/Banner'
import McvFeedToggler from '@/components/FeedToggler'
export default {
  name: 'McvHome',
  components: {McvFeedToggler, McvBanner, McvPopularTags, McvMainFeed},
  data() {
    return {
      apiUrl: '/articles',
    }
  },
}
</script>
