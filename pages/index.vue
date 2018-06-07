<template>
  <p>See meta[name="description"] element by devtools</p>
</template>

<script>
export default {
  head () {
    return {
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: this.mounted
            ? 'updated'
            : 'not updated yet'
        }
      ]
    }
  },

  data () {
    return {
      mounted: false
    }
  },

  mounted () {
    this.mounted = true
  }
}
</script>