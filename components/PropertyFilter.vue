<template>
  <div class="filter-container">
    <div class="row">
      <div class="col-md-2 col-12 mb-1 ">
        <multiselect v-model="operation" :options="operations"  placeholder="Buy or sell?"></multiselect>
      </div>
      <div class="col-md-4 col-12 mb-1 p-xs-0">
        <multiselect v-model="type" :options="types" :multiple="true" :limit="2" placeholder="Property type" label="en_name" track-by="en_name">
        </multiselect>

      </div>
      <div class="col-md-3 col-12 mb-1 p-xs-0">
        <autocomplete
          :search="search"
          placeholder="Search region"
          aria-label="Search region"
          :get-result-value="getResultValue"
        ></autocomplete>
      </div>
      <div class="col-md-1 col-6  mb-1 p-xs-0">
        <b-button block id="popover-target-1" variant="success">
          Price &#8364;
        </b-button>
        <b-popover target="popover-target-1" triggers="focus" placement="top">
          <div class="row">
            <div class="col-md-6 pr-0">
              <b-form-input type="number" v-model="minprice" placeholder="Min price"></b-form-input>
            </div>
            <div class="col-md-6">
              <b-form-input type="number" v-model="maxprice" placeholder="Max price"></b-form-input>
            </div>
            <div class="col-md-12">
              <span class="price-window-text">{{ priceText }} &#8364;</span>
            </div>
          </div>
        </b-popover>
      </div>
    </div>
  </div>
</template>

<script>
import Autocomplete from '@trevoreyre/autocomplete-vue'
import Multiselect from 'vue-multiselect'

export default {
  name: "PropertyFilter",
  components: {
    Autocomplete,
    Multiselect
  },
  data () {
    return {
      operation: null,
      operations: ['Buy', 'Sell', 'Rent'],
      type: [],
      types: [],
      minprice: null,
      maxprice: null
    }
  },
  async mounted() {
    this.types = await this.$axios.$get('/api/types')
  },
  computed: {
    priceText() {
      let text = '';
      if(this.minprice > 0) {
        text += 'From ' +this.minprice + ' '
      }
      if(this.maxprice > 0) {
        text += 'To '+this.maxprice
      }
      if(text.length < 1) {
        return '';
      } else {
        return text;
      }

    }
  },
  methods: {
    search(input) {
      const url = `http://127.0.0.1:8000/api/region/${encodeURI(input)}`+'%20'

      return new Promise((resolve) => {
        if (input.length < 0) {
          return resolve([])
        }

        fetch(url)
          .then((response) => response.json())
          .then((data) => {
            resolve(data)
          })
      })
    },
    getResultValue(result) {
      return result.en_name;
    },
  }
}
</script>

<style>
.autocomplete-input {
  background-color: #fff;
  padding: 8px 12px 8px 48px;
  border: 1px solid #00a75e;
}
.multiselect__tags {
  border: 1px solid #00a75e;
}
.price-window-text {
  color: #00a75e;
  display: block;
  font-weight: bold;
  text-align: center;
  padding: 5px 3px;
}
@media (min-width: 768px) {
  .p-xs-0 {
    padding-left: 0 !important;
  }
}
</style>
