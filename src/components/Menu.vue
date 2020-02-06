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

  <tbody v-for="item in getMenuItems" :key="item.name">
    <tr>
      <td> {{ item.name }} </td>      
    </tr>

    <tr>
      <td>{{ item.description }}</td>      
    </tr>

    <tr v-for="option in item.options" :key="option.size">
      <td>{{ option.size }}</td>
      <td>{{ option.price }}</td>
      <td>
        <button class="btn" type="button" v-on:click="addToBasket(item, option)">+</button>
      </td>
    </tr>
  </tbody>
</table>

</div>

<div class="basket">

<h3>basket</h3>

<div>

<table class="table table-hover">

  <tbody>
    <tr v-for="item in basket" :key="item.name+item.size">
      <td>
        <button type="button">-</button>
      </td>

      <td> {{ item.quantity }} </td>
      
      <td>
        <button type="button">+</button>
      </td>

      <td> {{ item.name }} </td>

      <td> {{ item.price }} </td>
    </tr>   
  </tbody>

</table>

</div>

</div>
 
</div>

</template>

<script>
export default {
  name: 'appMenu',
  data() {
    return {
      basket: [],

      getMenuItems: {
        1: {
          'name': 'Butter Pecan',
          'description': 'is a smooth vanilla ice cream with a slight buttery flavor',
          'options': [{
            'size': 9,
            'price': 6.95
          }, {
            'size': 12,
            'price': 10.95
          }]
        },
        2: {
          'name': 'Hokey pokey',
          'description': 'a flavour of ice cream in New Zealand, consisting of plain vanilla',
          'options': [{
            'size': 9,
            'price': 7.95
          }, {
            'size': 12,
            'price': 12.95
          }]
        },
        3: {
          'name': 'Pistachio ice cream',
          'description': 'also referred to as pistachio nut ice cream',
          'options': [{
            'size': 9,
            'price': 7.95
          }, {
            'size': 12,
            'price': 12.95
          }]
        }        
      }
    }
  },

  methods: {
    async addToBasket(item, option) {
      const iceExist = await this.basket.find(
        (icecream) => item.name === icecream.name && option.size === icecream.size        
      );
      
      if(iceExist) {
        iceExist.quantity++;

        return; 
      }

      this.basket.push({
        name: item.name,
        price: option.price,
        size: option.size,
        quantity: 1
      }) 
    }
  }  
}
</script>

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
