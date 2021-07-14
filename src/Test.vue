<template>
  <div>
    {{ foo }}
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import type {store as storeType} from './store'


export default defineComponent({
  props: ['foo', 'bar'],
  setup(){
    const x = new Array<storeType>()
  }
})
/*
line 8: 'storeType' is declared but its value is never read.Vetur(6133)
line 13: 'storeType' refers to a value, but is being used as a type here. Did you mean 'typeof storeType'?Vetur(2749)
 */
</script>