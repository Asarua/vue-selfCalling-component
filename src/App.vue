<template>
  <div>
    <demo :info="info" />
  </div>
</template>

<script>
import Demo from './components/Demo'
export default {
  data() {
    return {
      info: [
        {
          a: 1,
          b: 2,
          c: [
            {
              a: 11,
              c: {
                a: 111
              }
            }
          ]
        },
        {
          a: 3,
          b: 4
        }
      ]
    }
  },
  components: {
    Demo
  }
}
</script>
