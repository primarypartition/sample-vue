<template>
  <header>
    <div class="head_logo">
      <img src="#"/>
      <h1>ice cream</h1>
    </div>

    <nav>
    
    <ul>
      <li>
        <a href="/">Home</a>
      </li>
      <span>-</span>
    
      <li>
        <a href="/about">About</a>
      </li>
      <span>-</span>
    
      <li>
        <a href="/menu">Menu</a>
      </li>
      <span>-</span>
    
      <li>
        <a href="/contact">Contact</a>
      </li>
    </ul>
    
    </nav>  
  </header>  
</template>

<script>
export default {
  name: 'appHeader'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h1 {

}

.head_logo {

}

.head_logo img {

}

ul {
  padding: 10px 0;
}

li {
  display: inline-block; 
}

</style>
