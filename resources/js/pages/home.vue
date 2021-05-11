<template>
  <b-container>
    <b-row>
      <!-- Post item list -->
      <b-col sm="12" md="8">
        <post-item v-for="index in 3" :key="index" />
      </b-col>

      <!-- Right side panel-->
      <b-col
        md="4"
        class="d-none d-md-block"
      >
        <follow-item mode="me" :width="45" :height="45" />

        <!--Suggestion label-->
        <div>
          <b-row>
            <b-col sm="9">
              Suggestion for you
            </b-col>
            <b-col sm="3" class="text-right">
              See All
            </b-col>
          </b-row>
        </div>

        <follow-item
          v-for="index in 5"
          :key="index"
          mode="follow"
        />
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import PostItem from '../components/instagram/PostItem'
import FollowItem from '../components/instagram/FollowItem'

export default {

  components: {
    FollowItem,
    PostItem
  },

  middleware: 'auth',

  metaInfo () {
    return { title: this.$t('home') }
  }
}
</script>
