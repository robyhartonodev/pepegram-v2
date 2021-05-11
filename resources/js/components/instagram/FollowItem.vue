<template>
  <b-row align-v="center" class="my-2">
    <b-col sm="3">
      <b-img
        src="https://picsum.photos/30/30/?image=41"
        :width="width"
        :height="height"
        style="border-radius: 50px;"
      />
    </b-col>
    <b-col sm="6">
      <div>username</div>
      <div>name</div>
    </b-col>
    <b-col sm="3" class="text-right">
      <div v-if="mode === 'me'">
        Switch
      </div>
      <div v-if="mode === 'follow'">
        Follow
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: 'FollowItem',
  props: {
    mode: {
      type: String,
      default: 'follow' // possible value 'follow' or 'me'
    },
    height: {
      type: Number,
      default: 30
    },
    width: {
      type: Number,
      default: 30
    }
  }
}
</script>

<style scoped>

</style>
