<template>
  <div>
    <Header :title="title" />
    <nuxt />
  </div>
</template>

<script>
import Header from '@/components/Header'

export default {
  components: {
    Header
  },
  data(){
      return{
          title: ''
      }
  },
  created(){
      this.setListener()
  },
  methods:{
      setListener(){
          this.$nuxt.$on('updateHeader', this.setHeader)
      },
      setHeader(title){
          this.title = title || ''
      }
  }
}
</script>