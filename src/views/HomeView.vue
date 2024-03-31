<template>
    <div class="px-[16px] md:px-[42px]">
        <div class="mb-[50px]">
            <img :src="require('@/assets/images/homeheader.png')" class="object-cover w-full h-[180px] md:h-full" />
        </div>
        <div class="pb-[84px]">
            <h2 class="text-3xl font-semibold mb-[24px]">Kategori</h2>
            <div class="flex gap-4 flex-wrap lg:flex-nowrap overflow-x-auto">
                <a
          v-for="(v, i) in kategori"
          :key="i"
          :href="v.url"
          class="relative w-full rounded-2xl bg-no-repeat bg-cover bg-center h-[140px] cursor-pointer"
          :style="{ backgroundImage: `url(${v.img})`, boxShadow: '0px 4px 6px rgba(0, 0, 0, 0.1)' }"
        >
          <div class="absolute inset-0 flex flex-col justify-end z-20 px-[24px] pb-[24px]">
            <h3 class="text-white text-lg font-semibold">{{ v.nama }}</h3>
            <hr>
            <h3 class="text-white text-lg font-semibold">{{ v.jumlah }} Venue</h3>
          </div>
          <div class="absolute bg-black top-0 left-0 w-full h-full opacity-[0.3] rounded-2xl"></div>
          <div class="hover:transform hover:-translate-y-1 transition duration-300 ease-in-out absolute top-0 left-0 w-full h-full"></div>
        </a>
            </div>
        </div>
        <div class="pb-[24px] px-[50px]">
            <div class="flex items-center gap-4 flex-wrap lg:flex-nowrap">
               <div class="w-full lg:w-[50%]">
                <h3 class="text-3xl font-bold mb-[24px]">Sewa tempat <br/> dengan mudah dan <br/> cepat</h3>
                <p>
                    Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
                </p>
               </div>
               <div class="w-full lg:w-[50%]" >
                <img :src="require('@/assets/images/gambarkanan.png')" class="w-fit mx-auto" />
               </div>
            </div>
        </div>
        <div class="pb-[24px]">
        <div class="text-center py-[24px]">
            <h2 class="text-3xl font-bold mb-[14px]">Tempat Terbaik di tekMIRA</h2>
            <h3 class="text-md">Nikmati fasilitas layanan terbaik dari kami</h3>
        </div>
        <div class="flex items-center flex-wrap justify-center gap-8">
            <div v-for="(v, i) in dataTempat" :key="i" class="w-full md:w-[30%] rounded-2xl overflow-hidden bg-white shadow-md" style="height: auto;">
            <img :src="require('@/assets/images/'+v.img)" class="w-full h-60 object-cover" />
            <div class="p-4">
                <h4 class="text-md font-semibold">{{ v.nama }}</h4>
                <p class="text-sm">{{ truncateText(v.deskripsi, 100) }}</p>
                <div class="flex justify-end mt-[24px]">
                <a :href="v.kategori.includes('Ruang Rapat') ? '/meeting/'+v.slug :  v.kategori.includes('Wedding') ? '/wedding/'+v.slug : v.kategori.includes('tenis') ? '/tenis/'+v.slug :  '/wisma/'+v.slug" class="ml-auto text-sm text-rose-500 hover:underline hover:decoration-from-font">LOOK NOW!</a>
                </div>
            </div>
            </div>
        </div>
        </div>
    </div>
</template>

<script>
export default {
    metaInfo() {
    return {
      title: "Home",
      titleTemplate: "tekMIRA - %s",
    };
  },
    data() {
        return {
            kategori: [
                { nama: "Tenis", jumlah: 2, img: require('@/assets/images/kategori1.png'), url:'/tenis' },
                { nama: "Ruang Rapat", jumlah: 4, img: require('@/assets/images/kategori2.png'), url:'/meeting' },
                { nama: "Wisma", jumlah: 4, img: require('@/assets/images/kategori3.png'), url:'/wisma' },
                { nama: "Wedding/Seminar", jumlah: 2, img: require('@/assets/images/kategori4.png'), url:'/wedding' }
            ],
        };
    },
    computed: {
    dataTempat() {
      return this.$store.getters.dataTempat;
    },
  },
    methods:{
    truncateText(text, maxLength) {
      if (text && text.length > maxLength) {
        return text.slice(0, maxLength) + "...";
      }
      return text;
    },
    }
};
</script>

<style scoped>
/* Gaya lainnya */

/* Efek hover */
.cursor-pointer:hover {
  transform: translateY(-4px); /* Ubah nilai -5px sesuai keinginan */
}
</style>
