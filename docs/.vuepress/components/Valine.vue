<template>
  <div id="vcomments"></div>
</template>

<script>
export default {
  name: 'valine',
  mounted: function(){
    // require window 
    const Valine = require('valine');
    if (typeof window !== 'undefined') {
      this.window = window
      window.AV = require('leancloud-storage')
      
    }
     
    new Valine({
      el: '#vcomments' ,
      appId: '5yDexh0gcXFTRwSYN93e1FlO-gzGzoHsz',// your appId
      appKey: '3A1nGxssaJSwUNUPgRkzV5Ha', // your appKey
      notify: true, 
      verify: false, 
      avatar: 'fy', 
      placeholder: 'just go go' 
    });
  },
}
</script>

