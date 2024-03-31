<template>
	<footer class="z-40 bg-[#013068] shadow-lg px-[16px] md:px-[42px] py-[34px]">
		<div class="flex justify-between gap-8 flex-wrap">
			<div class="flex flex-col w-full md:w-1/2 lg:w-1/4 gap-8">
				<h4 class="text-white font-semibold text-xl">Informasi</h4>
				<div class="flex flex-col gap-4">
				<a href="#" class="text-white font-semibold text-md">Situs Utama</a>
				<a href="#" class="text-white font-semibold text-md">Hubungi Kami</a>
				<a href="#" class="text-white font-semibold text-md">Cara Bayar</a>
			</div>
			</div>
			<div class="flex flex-col w-full md:w-1/2 lg:w-1/4 gap-8">
				<h4 class="text-white font-semibold text-lg">Tautan Terkait</h4>
				<div class="flex flex-col gap-4">
				<p class="text-white font-semibold text-sm">Kementerian ESDM</p>
				<p class="text-white font-semibold text-sm">Direktorat Jenderal Mineral dan Batubara</p>
			</div>
			</div>
			<div class="flex flex-col w-full md:w-1/2 lg:w-1/4 gap-8">
				<h4 class="text-white font-semibold text-lg">Balai Besar Pengujian Mineral dan Batubara (BBPMB)</h4>
				<div class="flex flex-col gap-4">
				<p class="text-white font-semibold text-sm">Jalan Jend. Sudirman No.623, Wr. Muncang, Kec. Bandung Kulon, Kota Bandung, Jawa Barat 40211</p>
				<p class="text-white font-semibold text-sm">(022) 6030483</p>
				<a href="#" class="text-white font-semibold text-sm">info.tekmira@esdm.go.id</a>
			</div>
			</div>
			<div class="flex flex-col md:w-1/2 lg:w-1/6 gap-8">
				<h4 class="text-white font-semibold text-xl">Media Sosial</h4>
				<div class="flex gap-4">
				<a href="#" class="text-white font-semibold text-md"><img :src="require('@/assets/icons/fb.png')" class="object-fill w-full h-full" /></a>
				<a href="#" class="text-white font-semibold text-md"><img :src="require('@/assets/icons/x.png')" class="object-fill w-full h-full" /></a>
				<a href="#" class="text-white font-semibold text-md"><img :src="require('@/assets/icons/ig.png')" class="object-fill w-full h-full" /></a>
				<a href="#" class="text-white font-semibold text-md"><img :src="require('@/assets/icons/yt.png')" class="object-fill w-full h-full" /></a>
				<a href="#" class="text-white font-semibold text-md"><img :src="require('@/assets/icons/tt.png')" class="object-fill w-full h-full" /></a>
			</div>
			</div>
		</div>
	</footer>
</template>

<script>
export default {
	methods: {
		logout() {
			localStorage.clear();
			this.$router.push('/login');
		},
	},
};
</script>