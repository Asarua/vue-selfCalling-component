<template>
  <div>
    <div v-for="(item, index) in getArray" :key="index">
      <el-button>
        {{item.a}}
      </el-button>
      <div v-if="!!item.c">
        <demo :info="item.c" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'demo',
  props: {
    info: {
      type: [Object, Array]
    }
  },
  computed: {
    getArray() {
      const { info } = this
      return Array.isArray(info) ? info : [info]
    }
  },
}
</script>
