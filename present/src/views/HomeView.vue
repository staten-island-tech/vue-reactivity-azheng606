<template>
  <div>
    <DestCard v-for ="destination in destinations" 
    :key="destination.name" 
    :Destination="destination"/> 
  </div>
</template>

<script setup>
import DestCard from "@/components/DestCard.vue";
const destinations = [
        {
          name: "iphone SE",
          price: "$429",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/iphone-se-finish-unselect-gallery-1-202207?wid=5120&hei=2880&fmt=p-jpg&qlt=80&.v=1655249921393"
        },
        {
          name: "iphone 13",
          price: "$599",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/iphone-13-finish-unselect-gallery-1-202207_GEO_US?wid=5120&hei=2880&fmt=p-jpg&qlt=80&.v=1654894184756"
        },
        {
          name: "iphone 14",
          price: "$699",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/iphone-14-finish-select-202209-6-1inch_GEO_US?wid=2560&hei=1440&fmt=p-jpg&qlt=80&.v=1676506020026,"
        },
        {
          name: "iphone 15",
          price: "$799",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/iphone-15-model-unselect-gallery-2-202309_GEO_US?wid=2560&hei=1440&fmt=p-jpg&qlt=80&.v=1692925254305"
        },
        {
          name: "iphone 15 pro",
          price: "$999",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/iphone-15-pro-model-unselect-gallery-2-202309_GEO_US?wid=2560&hei=1440&fmt=p-jpg&qlt=80&.v=1693010535312"
        },
        {
          name: "ipad mini",
          price: "$499",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-mini-finish-unselect-gallery-1-202207?wid=2560&hei=1440&fmt=p-jpg&qlt=95&.v=1654903896391"
        },
        {
          name: "ipad 9th generation",
          price: "$329",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-finish-unselect-gallery-1-202207?wid=2560&hei=1440&fmt=p-jpg&qlt=95&.v=1654902561778"
        },
        {
          name: "ipad 10th generation",
          price: "$449",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-10th-gen-finish-unselect-gallery-1-202212?wid=2560&hei=1440&fmt=p-jpg&qlt=95&.v=1667592106064"
        },
        {
          name: "ipad air",
          price: "$599",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-air-finish-unselect-gallery-1-202207?wid=2560&hei=1440&fmt=p-jpg&qlt=95&.v=1654902977555"
        },
        {
          name: "ipad pro",
          price: "$799",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/ipad-pro-model-select-gallery-1-202212?wid=2560&hei=1440&fmt=p-jpg&qlt=95&.v=1667594167948"
        },
        {
          name: "iMac",
          price: "$1299",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/imac-24-no-id-blue-selection-hero-202310?wid=452&hei=420&fmt=jpeg&qlt=95&.v=1701459101618"
        },
        {
          name: "Macbook Pro 14' ",
          price: "$1599",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/mac-card-40-macbookpro-14-16-202310_GEO_US?wid=600&hei=500&fmt=p-jpg&qlt=95&.v=1699558878362"
        },
        {
          name: "Macbook Air 13' ",
          price: "$1099",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/mac-card-40-macbook-air-13-15-202306?wid=600&hei=500&fmt=p-jpg&qlt=95&.v=1684262493564"
        },
        {
          name: "Apple Vision Pro ",
          price: "$3499",
          img: "https://store.storeimages.cdn-apple.com/4982/as-images.apple.com/is/vision-pro-card-66-vision-pro-202401?wid=1172&hei=588&fmt=p-jpg&qlt=95&.v=1702510799485"
        },
      ]
</script>

<style scoped>

</style>