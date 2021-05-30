<template>
  {{text}}
</template>

<script setup>
import { defineProps, reactive } from 'vue'

defineProps({
  msg: String
})

const state = reactive({ count: 0 })

import {Sitdown} from 'sitdown'

const text = (new Sitdown()).HTMLToMD('<h1>Hello World</h1>')
</script>
