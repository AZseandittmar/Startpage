<template>
</template>

<script>
  export default {
    name: "LinkGroup",
    data() {
      return {
        links: [
          {
            url: 'https:/www.example.com',
            name: 'example.com',
            desc: 'this is the description',
            datetime: '01/01/2001 01:01:01am'
          }
        ],
        linkCount: 1,
        
        mounted() {
          if (localStorage.getItem('linkCount') {
            this.linkCount = localStorage.getItem('linkCount')
            loadLinks()
          }
        },
        
        unmounted() {
          localStorage.setItem('linkCount', this.links.count)
          saveLinks()
        },
        
        methods: {
          saveLinks() {
            parsed = JSON.stringify(this.links)
            localStorage.setItem('links',parsed)
          },
          loadLinks() {
            this.links = JSON.parse(localStorage.getItem('links'))
          }
        } 
      }
    }
</script>
<style></style>
