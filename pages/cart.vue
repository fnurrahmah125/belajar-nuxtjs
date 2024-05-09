<template>
  <div class="min-h-screen container mx-auto py-10">
    <h1 class="text-4xl font-medium">Cart</h1>
    <div>
      <table class="table-auto text-center w-full">
        <thead>
          <tr>
            <th class="py-6 text-left">Product Details</th>
            <th>Quantity</th>
            <th>Price</th>
            <th>Total</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in items" :key="item.id">
            <td class="pb-4">
              <div class="flex items-center gap-4">
                <img :src="item.image" class="h-20 w-20 rounded-md" />
                <div class="font-medium">{{ item.name }}</div>
              </div>
            </td>
            <td>
              <div class="flex items-center gap-4 justify-center">
                <button
                  class="px-2 border border-neutral-600 rounded-md text-xl"
                  @click="decrease(item)"
                >
                  -</button
                ><span>{{ item.count }}</span
                ><button
                  class="px-2 border border-neutral-600 rounded-md text-xl"
                  @click="increase(item)"
                >
                  +
                </button>
              </div>
            </td>
            <td>${{ item.price.toFixed(2) }}</td>
            <td>$ {{ (item.count * item.price).toFixed(2) }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: 1,
          name: "ClassicComfort Tee",
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSz1Jz8NB_MYh86X1F2oRW7Pb9GE1Z4upD2jpH-n92KPDabB3y85SO5EheBGRSFBanU4iE&usqp=CAU",
          price: 39,
          count: 0,
        },
        {
          id: 2,
          name: "EverydayEssentials Shirt",
          image:
            "https://unboundmerino.com/cdn/shop/files/mega-menu-our-promise-page_1440x.jpg?v=1667743361",
          price: 54,
          count: 0,
        },
        {
          id: 3,
          name: "SimpleStyle Top",
          image: "https://ae01.alicdn.com/kf/HTB1ZPO5ci6guuRjy0Fmq6y0DXXaI.jpg",
          price: 20,
          count: 0,
        },
        {
          id: 4,
          name: "BasicBlend T-Shirt",
          image:
            "https://lp2.hm.com/hmgoepprod?set=source[/62/6d/626df1a5f1793065a5d3d2378e6e0a4da67edb72.jpg],origin[dam],category[men_tshirtstanks_multipacks],type[DESCRIPTIVESTILLLIFE],res[z],hmver[2]&call=url[file:/product/main]",
          price: 43,
          count: 0,
        },
      ],
    };
  },
  methods: {
    increase(item) {
      item.count++;
    },
    decrease(item) {
      if (item.count > 0) {
        item.count--;
      }
    },
  },
};
</script>
