<template>
  <div>
    <h2 class="text-center text-2xl font-bold">Kirim Paket Makin Singkat</h2>
    <p class="text-center mt-5 text-gray-500">
      Masih kurang? Yuk explore sekarang biar ngga penasaran
    </p>
    <div class="block lg:flex gap-6 mt-16">
      <div class="w-full">
        <img
          src="https://kiriminaja.com/assets/banner-home-2.png"
          class="w-full h-auto"
          alt=""
        />
      </div>
      <div class="w-full mt-10 lg:mt-0">
        <div
          class="p-5 bg-purple-50 border-white border-2 flex gap-4 items-center"
          v-for="content in features"
        >
          <div class="w-8">
            <svg class="svg-icon text-purple-700" stroke="currentColor" fill="currentColor" viewBox="0 0 20 20">
              <path
                d="M10.219,1.688c-4.471,0-8.094,3.623-8.094,8.094s3.623,8.094,8.094,8.094s8.094-3.623,8.094-8.094S14.689,1.688,10.219,1.688 M10.219,17.022c-3.994,0-7.242-3.247-7.242-7.241c0-3.994,3.248-7.242,7.242-7.242c3.994,0,7.241,3.248,7.241,7.242C17.46,13.775,14.213,17.022,10.219,17.022 M15.099,7.03c-0.167-0.167-0.438-0.167-0.604,0.002L9.062,12.48l-2.269-2.277c-0.166-0.167-0.437-0.167-0.603,0c-0.166,0.166-0.168,0.437-0.002,0.603l2.573,2.578c0.079,0.08,0.188,0.125,0.3,0.125s0.222-0.045,0.303-0.125l5.736-5.751C15.268,7.466,15.265,7.196,15.099,7.03"
              ></path>
            </svg>
          </div>
          <div class="w-full text-gray-500">{{ content.text }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      features: [
        {
          text: 'Berbagai service expedisi sameday, kargo dan lainnya.'
        },
        {
          text: 'Penjemputan paket tanpa minimal kiriman.'
        },
        {
          text: 'Fitur dropoff atau cashless.'
        },
        {
          text: 'Kirim paket COD dengan pencairan tercepat.'
        },
        {
          text: 'Platform mudah digunakan (user friendly).'
        },
        {
          text: 'Meminimalisir rasio retur.'
        },
      ]
    }
  }
}
</script>
