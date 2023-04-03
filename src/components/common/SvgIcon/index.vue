<!--
 * @Description:
 * @version:
 * @author: sueRimn
 * @Date: 2023-04-03 18:46:47
 * @LastEditors: sueRimn
 * @LastEditTime: 2023-04-03 19:18:29
-->
<script setup lang='ts'>
import { computed, useAttrs } from 'vue'
import { Icon } from '@iconify/vue'

interface Props {
  Icon?: string
}

defineProps<Props>()

const attrs = useAttrs()

const bindAttrs = computed<{ class: string; style: string }>(() => ({
  class: (attrs.class as string) || '',
  style: (attrs.style as string) || '',
}))
</script>

<template>
  <Icon :icon="Icon" v-bind="bindAttrs" />
</template>
