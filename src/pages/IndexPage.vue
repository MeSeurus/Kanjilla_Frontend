<template>
<!--  <div class="q-pa-md">-->
<!--    <q-carousel-->
<!--      arrows-->
<!--      animated-->
<!--      v-model="slide"-->
<!--      height="400px"-->
<!--    >-->
<!--      <q-carousel-slide name="first" img-src="https://cdn.quasar.dev/img/mountains.jpg">-->
<!--        <div class="absolute-bottom custom-caption">-->
<!--          <div class="text-h2">First stop</div>-->
<!--          <div class="text-subtitle1">Mountains</div>-->
<!--        </div>-->
<!--      </q-carousel-slide>-->
<!--      <q-carousel-slide name="second" img-src="https://cdn.quasar.dev/img/parallax1.jpg">-->
<!--        <div class="absolute-bottom custom-caption">-->
<!--          <div class="text-h2">Second stop</div>-->
<!--          <div class="text-subtitle1">Famous City</div>-->
<!--        </div>-->
<!--      </q-carousel-slide>-->
<!--      <q-carousel-slide name="third" img-src="https://cdn.quasar.dev/img/parallax2.jpg">-->
<!--        <div class="absolute-bottom custom-caption">-->
<!--          <div class="text-h2">Third stop</div>-->
<!--          <div class="text-subtitle1">Famous Bridge</div>-->
<!--        </div>-->
<!--      </q-carousel-slide>-->
<!--    </q-carousel>-->
<!--  </div>-->

  <div class="my-table">
    <q-timeline color="secondary">
      <q-timeline-entry heading body="Timeline heading" />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        avatar="https://cdn.quasar.dev/img/avatar3.jpg"
        :body="body"
      />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 21, 1986"
        icon="delete"
        :body="body"
      />

      <q-timeline-entry heading body="November, 2017" />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        :body="body"
      />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        :body="body"
      />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        color="orange"
        icon="done_all"
        :body="body"
      />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        :body="body"
      />

      <q-timeline-entry
        title="Event Title"
        subtitle="February 22, 1986"
        :body="body"
      />
    </q-timeline>
  </div>
</template>

<script>
import { defineComponent } from 'vue'
// import { ref } from 'vue'

export default defineComponent({
  name: 'IndexPage',

  setup () {
    return {
      // slide: ref('first'),
      body: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
    }
  }
})
</script>
