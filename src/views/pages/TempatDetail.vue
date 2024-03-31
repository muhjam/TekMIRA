<template>
    <div v-if="detailTempat" class="px-[16px] md:px-[42px]">
      <div class="pb-[24px]">
            <div class="flex items-center gap-4 mt-[24px] pb-[12px]">
              <h3 class="text-3xl font-bold">{{ detailTempat.nama }}</h3>
            </div>
            <div class="flex items-center gap-2 md:gap-4 mt-[24px] pb-[34px]">
            <div class="w-[70%] h-[500px] rounded-l-[50px] overflow-hidden">
              <img :src="require('@/assets/images/'+detailTempat.img)" class="object-cover w-full h-full rounded-l-[50px]" />
            </div>
            <div class="w-[30%] flex flex-col justify-end gap-2 md:gap-4">
              <div class="flex gap-2 md:gap-4 flex-col">
                <div class="w-full flex justify-end">
                  <div class="w-full rounded-tr-[50px] overflow-hidden">
                    <img :src="require('@/assets/images/'+detailTempat.img)" class="object-cover w-full h-[240px] rounded-tr-[50px]" />
                  </div>
                </div>
                <div class="w-full flex justify-end">
                  <div class="w-full rounded-br-[50px] overflow-hidden">
                    <img :src="require('@/assets/images/'+detailTempat.img)" class="object-cover w-full h-[240px] rounded-br-[50px]" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="pb-[54px]">
            <div class="flex gap-4 flex-wrap lg:flex-nowrap">
              <div class="flex flex-col w-full justify-start gap-8 border-solid border-t-[2px] border-gray-300 py-[24px]">
                 <p>{{ detailTempat.deskripsi }}</p>
                  <a :href="`http://wa.me/6285795111965?text=Hallo%20mimin%20TekMIRA,%20saya%20mau%20booking%20tempat%20${detailTempat.kategori}.`" target="_blank" class="px-[34px] py-[16px] md:px-[82px] md:py-[16px] rounded-md bg-white hover:opacity-[0.8] w-fit flex items-center gap-2"><img :src="require('@/assets/icons/wa.png')" class="inline w-[24px] h-[24px]" />BOOK NOW!</a>
              </div>
              <div class="w-full lg:w-1/2 flex flex-col gap-4">
               <div class="flex items-start w-full px-[24px] py-[24px] bg-white shadow-sm rounded-xl">
                  <div class="w-1/2 md:w-1/3">
                    <h3 class="text-sm md:text-md  font-semibold mb-[6px]">Ukuran</h3>
                    <p>{{ detailTempat.spesifikasi.ukuran }}</p>
                  </div>
                  <div class="w-1/3 hidden md:block">
                    <h3 class="text-md  font-semibold mb-[6px]">Hubungi</h3>
                    <p>{{ detailTempat.spesifikasi.hubungi }}</p>
                  </div>
                  <div class="w-1/2 md:w-1/3">
                    <h3 class="text-md  font-semibold mb-[6px]">Total Kapasitas</h3>
                    <p>{{ detailTempat.spesifikasi.kapasitas }} Orang</p>
                  </div>
               </div>
               <div class="w-full px-[24px] py-[24px] bg-white shadow-sm rounded-xl">
                    <h3 class="text-md md:text-lg  font-semibold mb-[6px]">Fasilitas Utama</h3>
                  <div class="flex flex-wrap">
                  <div v-for="(v, i) in detailTempat.fasilitas" :key="i" class="w-1/2 flex mb-[8px] gap-4">
                    <img :src="require('@/assets/icons/'+ v + '.png')" class="object-contain" />
                    <p>{{ v }}</p>
                  </div>
                </div>
               </div>
            </div>
          </div>
        </div>
        <div class="pb-[54px]">
            <div class="flex flex-col gap-2">
              <div class="flex items-center gap-4">
              <h2 class="text-3xl font-semibold">Lihat Ruangan Lainnya</h2>
              <img :src="require('@/assets/icons/right-arrow.png')" class="object-cover" />
            </div>
              <div class="flex items-center gap-8 flex-wrap md:flex-nowrap">
            <div v-for="(v, i) in tempatLain" :key="i" class="w-full md:w-1/3 rounded-2xl overflow-hidden bg-white shadow-md" style="height: auto;">
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
        <div class="pb-[54px]">
            <div class="flex flex-col gap-2">
              <h2 class="text-3xl font-semibold">Lokasi</h2>
              <div class="flex gap-2">
              <img :src="require('@/assets/icons/lokasi.png')" class="object-contain" />
              <h3>{{ detailTempat.lokasi }}</h3>
            </div>
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3960.7675326119415!2d107.5765414750902!3d-6.918371767713968!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2e68e606d1d99309%3A0x258f2b35fa2ac2ac!2sBBPMB%20tekMIRA!5e0!3m2!1sen!2sid!4v1711814411862!5m2!1sen!2sid" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
          </div>
        </div>
    </div>
    <div v-else>
        <ErrorPage></ErrorPage>
    </div>
</template>

<script>
import ErrorPage from "@/views/pages/Error/404.vue";

export default {
  components: {
    ErrorPage,
  },
    metaInfo() {
    return {
      title: "Meeting",
      titleTemplate: "tekMIRA - %s",
    };
  },
    computed: {
      detailTempat() {
      return this.$store.state.detailTempat;
    },
    tempatLain() {
        return this.$store.state.tempatLain;
      },
  },
  async mounted(){
   await this.getData();
  },
    methods:{
      async getData(){
        await this.$store.dispatch('fetchDetailTempat', this.$route.params.slug);
      await this.$store.dispatch('fetchKategoriTempat', this.detailTempat.kategori); // Ambil kategori dari detailTempat
      await this.$store.dispatch('fetchTempatLain', {
        slug: this.$route.params.slug,
        kategori: this.detailTempat.kategori // Gunakan kategori dari detailTempat
      });

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
