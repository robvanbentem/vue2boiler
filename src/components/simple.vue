<template>
  <div class="card">
    <div class="card-header">
      Simple page
    </div>
    <div class="card-block">
      <div v-if="loading">
        Simsalabim boem bam, die hele pagina laad ik omdat het kan!
      </div>
      <div v-if="!loading">
        {{ msg }}
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'simple',
  data () {
    return {
      loading: true,
      msg: 'Hello vue!'
    }
  },
  components: {},
  created () {
    this.load()
  },
  watch: {
    '$route': function () {
      console.log('test')
      this.load()
    }
  },
  methods: {
    load () {
      setTimeout(() => {
        this.msg = 'hehehe'
        this.loading = false
      }, 2000)
    }
  }
}
</script>
<style scoped lang="sass">
</style>