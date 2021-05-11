<template>
  <b-card
    class="mb-3"
    header-tag="header"
    footer-tag="footer"
    body-class="p-0"
    footer-class="p-0"
  >
    <template #header>
      <b-row align-v="center">
        <b-col sm="1">
          <b-img
            src="https://picsum.photos/30/30/?image=41"
            :width="30"
            :height="30"
            class="clickable"
            style="border-radius: 50px"
          />
        </b-col>
        <b-col sm="10">
          <div>username</div>
          <div>location</div>
        </b-col>
        <b-col sm="1" class="text-right">
          <b-icon
            icon="three-dots"
            class="clickable"
            @click="() => {}"
          />
        </b-col>
      </b-row>
    </template>

    <b-card-img
      src="https://picsum.photos/400/400/?image=54"
      alt="Image"
      :width="415"
      :height="540"
    />

    <b-card-body>
      <!--Action Bars-->
      <b-row align-v="center">
        <b-col sm="11" align-self="center">
          <b-icon icon="heart" size="md" class="clickable mr-1" />
          <b-icon icon="chat" size="md" class="clickable mr-1" />
          <b-icon icon="share" size="md" class="clickable" />
        </b-col>
        <b-col sm="1">
          <b-icon icon="bookmark" size="md" class="clickable" />
        </b-col>
      </b-row>
      <!--Liked by-->
      <b-row>
        <b-col>Liked by man1, man2 and others</b-col>
      </b-row>
      <!--Comments-->
      <b-row>
        <b-col sm="12">
          username1: comment1
        </b-col>
        <b-col sm="12">
          username2: comment2
        </b-col>
        <b-col sm="12">
          username3: comment3
        </b-col>
      </b-row>
      <!--Post age-->
      <b-row>
        <b-col sm="12">
          777 HOURS AGO
        </b-col>
      </b-row>
    </b-card-body>

    <template #footer>
      <!--My comment input-->
      <b-row>
        <b-col sm="12">
          <b-input-group>
            <template #prepend>
              <span class="fa fas fa-emoji-smile" />
            </template>

            <b-form-input placeholder="Add a comment..." />

            <template #append>
              <b-btn>Post</b-btn>
            </template>
          </b-input-group>
        </b-col>
      </b-row>
    </template>
  </b-card>
</template>

<script>
export default {
  name: 'PostItem'
}
</script>

<style scoped>
.clickable {
  cursor: pointer;
}
</style>
