<template>
  <q-layout view="hHr lpR fFf">
    <q-header reveal elevated>
      <q-toolbar>

        <q-toolbar-title
          class="my-logo-header">
          Kanjilla
        </q-toolbar-title>

        <q-space/>

        <q-btn class="my-logo-header" stretch flat @click="goToMainPage" label="Main" />

        <q-space/>

        <q-btn-dropdown class="my-logo-header" stretch flat label="Kanji">
          <q-list class="my-japanese-text">
            <q-item-label header>JLPT level</q-item-label>
            <q-item clickable v-close-popup tabindex="0" @click="goToKanjiJ5">
              <q-item-section avatar>
                <q-avatar text-color="white" color="primary">N5</q-avatar>
              </q-item-section>
              <q-item-section>
                <q-item-label>Basic</q-item-label>
                <q-item-label caption>80 Kanji</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-close-popup tabindex="0">
              <q-item-section avatar>
                <q-avatar text-color="white" color="primary">N4</q-avatar>
              </q-item-section>
              <q-item-section>
                <q-item-label>Elementary</q-item-label>
                <q-item-label caption>170 Kanji</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-close-popup tabindex="0">
              <q-item-section avatar>
                <q-avatar text-color="white" color="primary">N3</q-avatar>
              </q-item-section>
              <q-item-section>
                <q-item-label>Intermediate</q-item-label>
                <q-item-label caption>370 Kanji</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-close-popup tabindex="0">
              <q-item-section avatar>
                <q-avatar text-color="white" color="primary">N2</q-avatar>
              </q-item-section>
              <q-item-section>
                <q-item-label>Pre-Advanced</q-item-label>
                <q-item-label caption>380 Kanji</q-item-label>
              </q-item-section>
            </q-item>
            <q-item clickable v-close-popup tabindex="0">
              <q-item-section avatar>
                <q-avatar text-color="white" color="primary">N1</q-avatar>
              </q-item-section>
              <q-item-section>
                <q-item-label>Advanced</q-item-label>
                <q-item-label caption>1136 Kanji</q-item-label>
              </q-item-section>
            </q-item>
            <q-separator inset spaced />
          </q-list>
        </q-btn-dropdown>

        <q-separator dark vertical />
        <q-btn-dropdown class="my-logo-header" stretch flat label="Grammar" />

        <q-separator dark vertical />
        <q-btn class="my-logo-header" stretch flat label="Keigo" />

        <q-space/>

        <div class="my-japanese-text">Dark Mode
          <q-toggle
            v-model="third"
            checked-icon="check"
            color="grey-10"
            unchecked-icon="clear"
            @click="toggleDarkTheme"
          />
        </div>

        <q-btn
          flat
          dense
          round
          icon="account_circle"
          @click="toggleRightDrawer"
        />

      </q-toolbar>

    </q-header>

    <q-drawer
      v-model="rightDrawerOpen"
      side="right"
      overlay behavior="mobile"
      elevated
    >
      <q-list>
        <q-item-label
          header
        >
          Essential Links
        </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import { useQuasar } from 'quasar'
import EssentialLink from 'components/EssentialLink.vue'
import {useRouter} from "vue-router";

const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev'
  },
  {
    title: 'Github',
    caption: 'github.com/quasarframework',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    title: 'Discord Chat Channel',
    caption: 'chat.quasar.dev',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    title: 'Forum',
    caption: 'forum.quasar.dev',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  },
  {
    title: 'Twitter',
    caption: '@quasarframework',
    icon: 'rss_feed',
    link: 'https://twitter.quasar.dev'
  },
  {
    title: 'Facebook',
    caption: '@QuasarFramework',
    icon: 'public',
    link: 'https://facebook.quasar.dev'
  },
  {
    title: 'Quasar Awesome',
    caption: 'Community Quasar projects',
    icon: 'favorite',
    link: 'https://awesome.quasar.dev'
  }
]

export default defineComponent({
  name: 'MainLayout',

  components: {
    EssentialLink,
  },

  setup () {

    const rightDrawerOpen = ref(false)
    const $q = useQuasar()
    const router = useRouter()
    $q.dark.set(false)

    return {
      essentialLinks: linksList,
      rightDrawerOpen,
      third: ref(false),
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      },
      toggleDarkTheme () {
        $q.dark.toggle()
      },
      goToMainPage () {
        router.replace({ path: `/` })
      },
      goToKanjiJ5 () {
        router.replace({ path: `/kanji/jlpt5/` })
      }
    }
  }
})
</script>
