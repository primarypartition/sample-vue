<template>
<div class="menu_wrapper">
<div class="menu">

<h3>icecreams</h3>

<table class="table table-hover">
  <thead class="thead-default">
    <tr>
      <th>Size</th>
      <th>Price</th>
      <th>Add to basket</th>
    </tr>
  </thead>

  <tbody>
    <tr>
      <td>apple-ice-cream</td>      
    </tr>

    <tr>
      <td>apple-ice-cream</td>      
    </tr>

    <tr>
      <td>large</td>
      <td>$10</td>
      <td>
        <button class="btn btn-sm btn-outline-success" 
                type="button">+</button>
      </td>
    </tr>

    <tr>
      <td>apple-ice-cream</td>      
    </tr>

    <tr>
      <td>apple-ice-cream</td>      
    </tr>

    <tr>
      <td>large</td>
      <td>$10</td>
      <td>
        <button class="btn btn-sm btn-outline-success" 
                type="button">+</button>
      </td>
    </tr>

    <tr>
      <td>apple-ice-cream</td>      
    </tr>

    <tr>
      <td>apple-ice-cream</td>      
    </tr>

    <tr>
      <td>large</td>
      <td>$10</td>
      <td>
        <button class="btn btn-sm btn-outline-success" 
                type="button">+</button>
      </td>
    </tr>
  </tbody>
</table>

</div>

<div class="basket">

<h3>basket</h3>

</div>

</div>

</template>

<script>
export default {
  name: 'appMenu'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.menu_wrapper {
  display: flex;
  flex-direction: row;
}

.menu {
  max-width: 60%;
}

.basket {
  max-width: 35%;
}

</style>
