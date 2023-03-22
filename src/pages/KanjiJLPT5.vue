<template>
  <div class="my-table">
    <q-table class="my-japanese-text"
      title="JLPT N5 Kanji list"
      :rows="rows"
      :columns="columns"
      row-key="number"
      color="amber"
      :pagination="initialPagination"
    />
  </div>
</template>

<script>

import { defineComponent } from 'vue'

const columns = [
  {
    name: 'id',
    required: true,
    label: '№',
    align: "center",
    field: row => row.number,
    format: val => `${val}`
  },
  {
    name: 'desc',
    required: true,
    label: 'Kanji',
    align: 'center',
    field: row => row.name,
    format: val => `${val}`
  },
  { name: 'onyomi', align: 'center', label: 'Onyomi', field: 'onyomi'},
  { name: 'kunyomi', align: 'center', label: 'Kunyomi', field: 'kunyomi' },
  { name: 'meaning', align: 'center', label: 'Meaning', field: 'meaning' },
  { name: 'example', align: 'center', label: 'Example', field: 'example' }
]

const rows = [
  {
    number: 1,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 2,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 3,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 4,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 5,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 6,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 7,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 8,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 9,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 10,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 11,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 12,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 13,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 14,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 15,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 16,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 17,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 18,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 19,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 20,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 21,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 22,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 23,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 24,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 25,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 26,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 27,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 28,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 29,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 30,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 31,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 32,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 33,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 34,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 35,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 36,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 37,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 38,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 39,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 40,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 41,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 42,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 43,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 44,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 45,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 46,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 47,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 48,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 49,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 50,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 51,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 52,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 53,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 54,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 55,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 56,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 57,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 58,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 59,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 60,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 61,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 62,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 63,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 64,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 65,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 66,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 67,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 68,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 69,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 70,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  },
  {
    number: 71,
    name: '一',
    onyomi: 'いち',
    kunyomi: 'ひと－つ',
    meaning: 'one',
    example: '一人 (alone)'
  },
  {
    number: 72,
    name: '二',
    onyomi: 'に',
    kunyomi: 'ふた－つ',
    meaning: 'two',
    example: '二人 (couple)'
  },
  {
    number: 73,
    name: '三',
    onyomi: 'さん',
    kunyomi: 'みっ－つ',
    meaning: 'three',
    example: '三月 (March)'
  },
  {
    number: 74,
    name: '四',
    onyomi: 'し',
    kunyomi: 'よん, \nよっ－つ',
    meaning: 'four',
    example: '四季 (four seasons)'
  },
  {
    number: 75,
    name: '五',
    onyomi: 'ご',
    kunyomi: 'いつ－つ',
    meaning: 'five',
    example: '五分 (five minutes)'
  },
  {
    number: 76,
    name: '六',
    onyomi: 'ろく',
    kunyomi: 'むっ－つ, むい',
    meaning: 'six',
    example: '六日 (six days)'
  },
  {
    number: 77,
    name: '七',
    onyomi: 'しち',
    kunyomi: 'なな－つ, なの, なぬ',
    meaning: 'seven',
    example: '七日 (seven days)'
  },
  {
    number: 78,
    name: '八',
    onyomi: 'はち',
    kunyomi: 'やっ－つ, よう',
    meaning: 'eight',
    example: '八日 (eight days)'
  },
  {
    number: 79,
    name: '九',
    onyomi: 'きゅう, く',
    kunyomi: 'ここの－つ',
    meaning: 'nine',
    example: '九月 (September)'
  },
  {
    number: 80,
    name: '十',
    onyomi: 'じゅう',
    kunyomi: 'とお, とう',
    meaning: '10',
    example: '十指 (ten fingers)'
  }
]

export default defineComponent ({

  name: 'KanjiJLPT5',

  setup () {
    return {
      initialPagination: {
        sortBy: 'number',
        descending: false,
        page: 1,
        rowsPerPage: 25
        // rowsNumber: xx if getting data from a server
      },

      columns,
      rows
    }
  }
})
</script>

<style scoped>

</style>
