<template>
  <div class="min-h-screen container mx-auto py-10">
    <h1 class="text-4xl font-medium">Products</h1>
    <div class="flex flex-wrap gap-8 py-10">
      <Card v-for="item in items" :key="item.id" :item="item" />
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
        },
        {
          id: 2,
          name: "EverydayEssentials Shirt",
          image:
            "https://unboundmerino.com/cdn/shop/files/mega-menu-our-promise-page_1440x.jpg?v=1667743361",
          price: 54,
        },
        {
          id: 3,
          name: "SimpleStyle Top",
          image: "https://ae01.alicdn.com/kf/HTB1ZPO5ci6guuRjy0Fmq6y0DXXaI.jpg",
          price: 20,
        },
        {
          id: 4,
          name: "BasicBlend T-Shirt",
          image:
            "https://lp2.hm.com/hmgoepprod?set=source[/62/6d/626df1a5f1793065a5d3d2378e6e0a4da67edb72.jpg],origin[dam],category[men_tshirtstanks_multipacks],type[DESCRIPTIVESTILLLIFE],res[z],hmver[2]&call=url[file:/product/main]",
          price: 43,
        },
      ],
    };
  },
};
</script>
