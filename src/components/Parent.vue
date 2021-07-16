<template>
  <div>
    <h1>slot-1のみ</h1>
    <Child>
      <template v-slot:slot-1>parent-slot-1</template>
    </Child>
    <h1>slot-2のみ</h1>
    <Child>
      <template v-slot:slot-2>parent-slot-2</template>
    </Child>
    <h1>slot-1, slot-2</h1>
    <Child>
      <template v-slot:slot-1>parent-slot-1</template>
      <template v-slot:slot-2>parent-slot-2</template>
    </Child>
  </div>
</template>

<script>
  import { defineComponent } from '@vue/composition-api'
  import Child from './Child.vue'

  export default defineComponent({
    components: {
      Child,
    },
    setup() {},
  })
</script>
