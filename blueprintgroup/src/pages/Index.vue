<template>
  <Layout>
    <img :src="logo" />
    <div>
      <h1>noun [c] ˈblueprint’</h1>
    </div>
    <div class="typewriter">
      <p>A plan that describes how to do <br> or achieve something in the future</p>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Home'
  },
  data() {
    return {
      logo: require('~/NameLogo.svg')
    }    
  }
}
</script>

<style scoped>
h1 {
  color: #A06A46;
}
.typewriter p {
  color: #000;
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .15em solid orange; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: .15em; /* Adjust as needed */
  animation: 
    typing 3.5s steps(30, end),
    blink-caret .5s step-end infinite;
}

/* The typing effect */
@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: orange }
}


</style>
