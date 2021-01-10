<template>
  <div>
    {{ user }}
  </div>
</template>

<script>
export default {
  data () {
    return {
      user: null
    }
  },

  methods: {
    async getUser () {
      this.user = await this.$axios.$get('/api/user')
    }
  },

  mounted () {
    this.getUser()
  }
}
</script>
