<template>
  <div class="about">
    <div class="text-danger">
      ****กรุณากดยืนยันเพื่อยืนยันสินค้าที่ท่านเลือก****
    </div>
    <div class="row">
      <product
        v-for="(item, index) in SearchMenu"
        :key="index"
        :NameProduct="item.NameProduct"
        :img="item.img"
        :Price="item.Price"
        :id="index"

      />
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
import { mapGetters } from "vuex";
import Product from "../components/Product.vue";
export default {
  name: "Home",
  components: {
    Product,
  },
  computed: {
    ...mapGetters(["SearchMenu"]),
  },
};
</script>
