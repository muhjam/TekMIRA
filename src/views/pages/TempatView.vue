<template>
    <div class="px-[16px] md:px-[42px]">
      <div class="pb-[24px]">
            <div class="flex items-center gap-4 flex-wrap md:flex-nowrap mt-[24px] md:pb-[34px]">
               <div class="w-full md:w-1/2">
                <h3 class="text-3xl font-bold mb-[24px]">{{ judul }} tekMIRA</h3>
                <h4 class="text-md font-light mb-[24px]"><span class="font-semibold">{{ kategoriTempat.length }}</span> LOKASI / TEMPAT STRATEGIS</h4>
                <p v-if="$route.path.includes('/meeting')" class="text-sm font-light mb-[34px]">
                  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
                </p>
                <p v-else-if="$route.path.includes('/wedding')" class="text-sm font-light mb-[34px]">
                  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
                </p>
                <p v-else-if="$route.path.includes('/tenis')" class="text-sm font-light mb-[34px]">
                  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
                </p>
                <p v-else-if="$route.path.includes('/wisma')" class="text-sm font-light mb-[34px]">
                  Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
                </p>
                <a :href="`http://wa.me/6285795111965?text=Hallo%20admin%20TekMIRA,%20saya%20mau%20nanya-nanya%20dong.`" class="px-[24px] py-[16px] rounded-md bg-white hover:opacity-[0.8] flex items-center gap-2 w-fit"><img :src="require('@/assets/icons/wa.png')" class="inline w-[24px] h-[24px]" />HUBUNGI SEKARANG</a>
               </div>
               <div class="flex justify-end w-full md:w-1/2">
                <img v-if="$route.path.includes('/meeting')"  :src="require('@/assets/images/kategori2.png')" class="object-cover rounded-xl md:rounded-none md:rounded-r-xl w-full md:w-[80%] h-[500px]" />
                <img v-else-if="$route.path.includes('/wedding')"  :src="require('@/assets/images/kategori4.png')" class="object-cover rounded-xl md:rounded-none md:rounded-r-xl w-full md:w-[80%] h-[500px]" />
                <img v-else-if="$route.path.includes('/tenis')"  :src="require('@/assets/images/kategori1.png')" class="object-cover rounded-xl md:rounded-none md:rounded-r-xl w-full md:w-[80%] h-[500px]" />
                <img v-else-if="$route.path.includes('/wisma')"  :src="require('@/assets/images/kategori3.png')" class="object-cover rounded-xl md:rounded-none md:rounded-r-xl w-full md:w-[80%] h-[500px]" />
               </div>
            </div>
        </div>
        <div class="pb-[24px] md:pb-[34px]">
                <div v-if="$route.path.includes('/meeting')"
          class="relative w-full rounded-2xl bg-no-repeat bg-cover bg-center h-[180px]"
          :style="{ backgroundImage: `url(${require('@/assets/images/kategori2.png')})`, boxShadow: '0px 4px 6px rgba(0, 0, 0, 0.1)' }"
        >
            </div>
                <div v-else-if="$route.path.includes('/wedding')"
          class="relative w-full rounded-2xl bg-no-repeat bg-cover bg-center h-[180px]"
          :style="{ backgroundImage: `url(${require('@/assets/images/kategori4.png')})`, boxShadow: '0px 4px 6px rgba(0, 0, 0, 0.1)' }"
        >
            </div>
                <div
                v-else-if="$route.path.includes('/tenis')"
          class="relative w-full rounded-2xl bg-no-repeat bg-cover bg-center h-[180px]"
          :style="{ backgroundImage: `url(${require('@/assets/images/kategori1.png')})`, boxShadow: '0px 4px 6px rgba(0, 0, 0, 0.1)' }"
        >
            </div>
                <div
                v-else-if="$route.path.includes('/wisma')"
          class="relative w-full rounded-2xl bg-no-repeat bg-cover bg-center h-[180px]"
          :style="{ backgroundImage: `url(${require('@/assets/images/kategori3.png')})`, boxShadow: '0px 4px 6px rgba(0, 0, 0, 0.1)' }"
        >
            </div>
        </div>
        <div class="pb-[54px]">
            <div class="flex">
              <div class="flex flex-col w-full justify-start gap-4">
                <div v-for="(v, i) in kategoriTempat" :key="i" class="w-full rounded-2xl overflow-hidden bg-white shadow-sm flex">
                  <img class="w-1/4 rounded-2xl object-cover hidden md:block" :src="require('@/assets/images/'+v.img[0])" alt="Category Image">
                  <div class="w-full px-6 py-4">
                    <img class="w-full h-[200px] mb-2 rounded-2xl object-cover block md:hidden" :src="require('@/assets/images/'+v.img[0])" alt="Category Image">
                    <h2 class="font-bold text-xl">{{ v.nama }}</h2>
                    <p class="text-gray-700 text-sm mb-2">{{ truncateText(v.lokasi, 30) }}</p>
                    <p class="text-gray-700 text-sm mb-[34px]">
                      {{ truncateText(v.deskripsi, 500) }}
                    </p>
                    <div class="flex gap-2">
                    <a href="#" class="px-[34px] py-[8px] bg-white border-solid border-[#F4F3F0] border-[2px] rounded-full text-sm font-medium hover:opacity-[0.8]">Lokasi</a>
                    <a :href="getSlug + '/' + v.slug" class="px-[34px] py-[8px] bg-[#245785] text-white rounded-full text-sm font-medium hover:opacity-[0.8]">Selengkapnya</a>
                  </div>
                  </div>
                </div>
              </div>
               <div class="md:flex justify-end items-start w-1/2 hidden" >
                <datepicker 
                v-model="selectedDate" 
                format="yyyy-MM-dd" 
                :inline="true" 
                :disabled-dates="disabledDates"
                :highlighted="highlightedDates"
              ></datepicker>
               </div>
            </div>
        </div>
    </div>
</template>

<script>
import Datepicker from "vuejs-datepicker";


export default {
  components: {
    Datepicker,
  },
    metaInfo() {
    return {
      title: this.judul,
      titleTemplate: "tekMIRA - %s",
    };
  },
  data() {
    return {
      judul: '',
    };
  },
    computed: {
    kategoriTempat() {
      return this.$store.getters.kategoriTempat;
    },
    getSlug() {
      return this.$route.path;
    },
  },
  async mounted(){
   await this.getData();
  },
    methods:{
      async getData(){
        this.judul = this.$route.path.includes('/meeting') ? 'Ruang Rapat' : this.$route.path.includes('/wedding') ? 'Wedding' : this.$route.path.includes('/tenis') ? 'Tenis' : 'Wisma'  ;
        this.deskripsi = this.$route.path.includes('/meeting') ? 'Ruang Rapat' : this.$route.path.includes('/wedding') ? 'Wedding' : this.$route.path.includes('/tenis') ? 'Tenis' : 'Wisma'  ;
       await this.$store.dispatch('fetchKategoriTempat', this.judul);
    },
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
</style>
