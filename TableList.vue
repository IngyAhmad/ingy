<template>
    <div class="row">
      <div class="col-md-12">
        <div class="card">
          <paper-table :title="table1.title" :sub-title="table1.subTitle" :data="table1.data" :columns="table1.columns">

          </paper-table>
          <div class="topnav">

  <input type="text" v-model = "name" placeholder="Enter name of product..">
  <input type="text" v-model = "price" placeholder="Enter price of product..">
  <input type="text" v-model = "createdAt" placeholder="Enter creation date..">
  <input type="text" v-model = "updatedAt" placeholder="Enter update date..">
</div>

        </div>
        <div class="topnav">
<a class="active" href="#Search">Search</a>
<a href="#for">For</a>
<a href="#Product">Product</a>
<input type="text" placeholder="Search Here..">
</div>


        </div>
        <button class="Button1">
                  <slot>Product-Add</slot>
                  </button>
                  <div id = "app">
                  <v-header></v-header>
                  <v-button></v-button>
                  </div>
                  <div class="summary-delivery">
                                          <select name="delivery-collection" class="summary-delivery-selection">
                                              <option value="0" selected="selected">Bayern Munich Mug</option>
                                             <option value="collection">Bayern Munich Poster</option>
                                             <option value="first-class">Bayern Munich Ball Star</option>
                                             <option value="first-class">Bayern Munich T-shirt Star</option>
                                          </select>
                                        </div>

              <button class="Button2">
              <slot>Product-Update</slot>
              </button>

              <div class="summary-delivery">
                                      <select name="delivery-collection" class="summary-delivery-selection">
                                          <option value="0" selected="selected">Bayern Munich Mug</option>
                                         <option value="collection">Bayern Munich Poster</option>
                                         <option value="first-class">Bayern Munich Ball Star</option>
                                         <option value="first-class">Bayern Munich T-shirt Star</option>
                                      </select>
                                    </div>

              <button class="Button3">
              <slot>Product-Delete</slot>
              </button>
              <div id = "app">
              <v-header></v-header>
              <v-button></v-button>
              </div>
              <div class="summary-delivery">
                                      <select name="delivery-collection" class="summary-delivery-selection">
                                          <option value="0" selected="selected">Bayern Munich Mug</option>
                                         <option value="collection">Bayern Munich Poster</option>
                                         <option value="first-class">Bayern Munich Ball Star</option>
                                         <option value="first-class">Bayern Munich T-shirt Star</option>
                                      </select>
                                    </div>

                 <div>
                                          <form role="form" class="" @submit.prevent="createProduct">




                <div style="max-width:400px">
                    <button class="btn btn-primary btn-sm" style="height:50px">Create Product</button>
                </div>
                 </form>
            </div>

        <header id="site-header">
  <div class="container">
    <h1>Shopping cart <span>[</span> <em><a href="https://codepen.io/tag/rodeo-007" target="_blank">Enjoy :)</a></em> <span class="last-span is-open">]</span></h1>
  </div>
</header>

<div class="container">

  <section id="cart">
    <article class="product">
      <header>
        <a class="remove">
          <img src="https://images-na.ssl-images-amazon.com/images/I/41-qglxV2pL._SY355_.jpg">



        <h1>Bayern Munich Mug</h1>

        <h3>Remove product</h3>
      </a>
    </header>

    <div class="content">
    <button class="Button5">
    <slot>Quantity</slot>
    </button>
    <div id = "app">
    <v-header></v-header>
    <v-button></v-button>
    </div>


      </div>



        <h2 class="full-price">
          $30.008
        </h2>

        <h2 class="price">

        </h2>
      </footer>
    </article>

    <article class="product">
      <header>
        <a class="remove">
          <img src="http://www.dw.com/image/19232798_303.jpg">



        <h1>Bayern Munich Poster</h1>

        <h3>Remove product</h3>
        </a>
        </header>

        <div class="content">
        <button class="Button5">
        <slot>Quantity</slot>
        </button>
        <div id = "app">
        <v-header></v-header>
        <v-button></v-button>
        </div>

        <div title="You have selected this product to be shipped in the color red." style="top: 0" class="color red"></div>
        <div title="You have selected this product to be shipped sized Small."  style="top: 43px" class="type small"></div>
      </div>

      <footer class="content">



        <h2 class="full-price">
          $20.999
        </h2>

        <h2 class="price">

        </h2>
      </footer>
    </article>

    <article class="product">
      <header>
        <a class="remove">
          <img src="http://images.footballfanatics.com/FFImage/thumb.aspx?i=/productImages%2F_2824000%2Fff_2824010_full.jpg&w=600">



        <h1>Bayern Munich T-shirt</h1>

        <h3>Remove product</h3>
      </a>
      </header>

      <div class="content">

      <button class="Button5">
      <slot>Quantity</slot>
      </button>
      <div id = "app">
      <v-header></v-header>
      <v-button></v-button>
      </div>

      <button class="Button4">
      <slot>Size</slot>
      </button>
      <div id = "app">
      <v-header></v-header>
      <v-button></v-button>
      </div>

      <div title="You have selected this product to be shipped in the color blue." style="top: 0" class="color blue"></div>
      <div style="top: 43px" class="type small">Large</div>
      </div>

      <footer class="content">
        <h2 class="full-price">
          $100.00
        </h2>

        <h2 class="price">

        </h2>
      </footer>
    </article>

  </section>

</div>

<footer id="site-footer">
  <div class="container clearfix">

    <div class="left">
      <h2 class="subtotal">Subtotal: <span>$187</span></h2>
      <h3 class="tax">Taxes (5%): <span>$8.2</span></h3>
      <h3 class="shipping">Shipping: <span>$5.00</span></h3>
    </div>

    <div class="right">
      <h1 class="total">Total: <span>$200.2</span></h1>
      <a class="btn">Checkout</a>
    </div>

  </div>
</footer>


    </div>
</template>
<script>
  import PaperTable from 'components/UIComponents/PaperTable.vue'
  import axios from 'axios'
  const tableColumns = ['Id', 'Name', 'Price', 'CreatedAt', 'UpdatedAt', 'SellerName']
  const tableData = [{
    id: 1,
    name: 'Bayern Munich Mug',
    price: '$30.008',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Manuel Neuer'
  },
  {
    id: 2,
    name: 'Bayern Munich Poster',
    price: '$20.999',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Thomas Muller'
  },
  {
    id: 3,
    name: 'Bayern Munich Ball',
    price: '$20.999',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Frank Ribery'
  },
  {
    id: 4,
    name: 'Bayern Munich T-shirt',
    price: '$100.00',
    createdat: '2/3/2018',
    updatedat: '2/3/2018',
    sellername: 'Robert Lewandowski'
  }
  ]

  export default {
    components: {
      PaperTable
    },
    data () {
      return {
        table1: {
          title: 'Bayern Munich Store',
          subTitle: 'Mia San Mia',
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          title: 'Table on Plain Background',
          subTitle: 'Here is a subtitle for this table',
          columns: [...tableColumns],
          data: [...tableData]
        },
        name: '',
        price: '',
        createdAt: '',
        updatedAt: ''
      }
    },
    methods: {
      createProduct: function () {
        console.log(this.name)
        console.log(this.price)
        console.log(this.createdAt)
        console.log(this.updatedAt)
        axios.post('http://localhost:3000/api/product/createProduct',
          {
            'name': this.name,
            'price': this.price,
            'createdAt': this.createdAt,
            'updatedAt': this.updatedAt
          })
          .then(response => {})
          .catch(e => {
          })
      }
    }
}
</script>
<style>

</style>
