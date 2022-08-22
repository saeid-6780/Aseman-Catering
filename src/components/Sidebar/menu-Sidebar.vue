<template>
  <nav
    class=" block overflow-y-auto flex-row flex-nowrap overflow-hidden shadow-xl bg-white flex flex-wrap items-center justify-between relative  z-10 pt-4 px-2 menu-sidebar"
  >
    <div class="py-4 w-full" >
      <div class="mb-8 text-center " v-for="menuItem in menuItems" v-bind:key="menuItem">
        <img :src="menuItem.img" alt="" class="mx-auto mb-2 px-3"/>
        <p class="text-sm ">{{ menuItem.name }}</p>
      </div>
    </div>

  </nav>
</template>
); }

<script>


export default {
  data() {
    return {
      menuItems:[
        {
          img:process.env.BASE_URL+'img/home/kebab-i.png',
          name:'کباب',
        },{
          img:process.env.BASE_URL+'img/home/khoraak-i.png',
          name:'خوراک ها',
        },{
          img:process.env.BASE_URL+'img/home/khoresht-i.png',
          name:'خورش ها',
        },{
          img:process.env.BASE_URL+'img/home/chelo-i.png',
          name:'چلو و پلو',
        },{
          img:process.env.BASE_URL+'img/home/daryaei-i.png',
          name:'غذا دریایی',
        },{
          img:process.env.BASE_URL+'img/home/salad-i.png',
          name:'اشتها آور سالاد',
        },{
          img:process.env.BASE_URL+'img/home/nooshidaniha-i.png',
          name:'نوشیدنی ها',
        }
      ],
      collapseShow: "hidden",
    };
  },
  methods: {
    toggleCollapseShow: function (classes) {
      this.collapseShow = classes;
    },
  },
  components: {

  },
};
</script>
<style>
.menu-sidebar{width: 20%;border-radius: 20px;}
</style>