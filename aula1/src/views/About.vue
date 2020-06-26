<template>
  <div class="about">
    <h1>This is an about page</h1>
    <ul v-for="product in products":key="product.id">
    <li {{product. name} | {{product.price}}}</li>
    </ul>
  </div>
</template>
<script>
import axios from 'axios';

export default{
  data(){
    return{
      products:[],

    };
  },
  created:{
    this.getproducts();

  },
  methods:{
    getProducts(){
      const url = 'https://localhost:5000/products';
      axios.get(url)
      .then(response => {
        .this.products = response;
        console.log(response);
      });
    }
  },
};
</script>