<template>
  <div>
    <p class="text-center text-2xl font-bold mb-16">
      Untuk Semua Kebutuhan Pengiriman Paketmu
    </p>
    <div class="mt-3 grid grid-cols-2 lg:grid-cols-3 gap-6 justify-between">
      <div
        v-for="content in listMobilitas"
        class="w-full bg-purple-50 rounded border-purple-900"
      >
        <div class="w-full p-5">
          <div class="w-1/6 mb-5">
            <div
              class="d-inline-flex py-3 rounded-full bg-purple-900 text-purple-900 bg-opacity-10 flex justify-center"
            >
              <div v-html="icon[content.id]"></div>
            </div>
          </div>
          <p class="text-xl mb-3 font-bold">{{ content.title }}</p>
          <p class="text-gray-500 mb-3">
            {{ content.text }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icon: {
        integrasi: `<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-armchair-2" width="28" height="28" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.5" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M5 10v-4a3 3 0 0 1 3 -3h8a3 3 0 0 1 3 3v4"></path>
                                        <path d="M16 15v-2a3 3 0 1 1 3 3v3h-14v-3a3 3 0 1 1 3 -3v2"></path>
                                        <path d="M8 12h8"></path>
                                        <path d="M7 19v2"></path>
                                        <path d="M17 19v2"></path>
                                    </svg>`,
        ekspedisi: `<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-shield-check" width="28" height="28" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.5" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M9 12l2 2l4 -4"></path>
                                        <path d="M12 3a12 12 0 0 0 8.5 3a12 12 0 0 1 -8.5 15a12 12 0 0 1 -8.5 -15a12 12 0 0 0 8.5 -3"></path>
                                    </svg>`,
        otomatis: `<svg xmlns="http://www.w3.org/2000/svg" class="icon" width="28" height="28" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.5" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><polyline points="13 3 13 10 19 10 11 21 11 14 5 14 13 3"></polyline></svg>`,
        alwaysforu: `<svg xmlns="http://www.w3.org/2000/svg" class="icon" width="28" height="28" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="none" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <rect x="4" y="13" rx="2" width="4" fill-opacity="0.5" fill="currentColor" height="6"></rect>
                                        <rect x="16" y="13" rx="2" width="4" fill-opacity="0.5" fill="currentColor" height="6"></rect>
                                        <path d="M4 15v-3a8 8 0 0 1 16 0v3"></path>
                                        <path d="M18 19a6 3 0 0 1 -6 3"></path>
                                    </svg>`,
        actualreport: `<svg xmlns="http://www.w3.org/2000/svg" class="icon icon-tabler icon-tabler-clipboard-check" width="28" height="28" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.5" stroke-linecap="round" stroke-linejoin="round">
                                        <path stroke="none" d="M0 0h24v24H0z" fill="none"></path>
                                        <path d="M9 5h-2a2 2 0 0 0 -2 2v12a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-12a2 2 0 0 0 -2 -2h-2"></path>
                                        <rect x="9" y="3" width="6" height="4" rx="2"></rect>
                                        <path d="M9 14l2 2l4 -4"></path>
                                    </svg>`,
        friendly: `<svg xmlns="http://www.w3.org/2000/svg" class="icon" width="28" height="28" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" fill="currentColor" fill-opacity="0.5" stroke-linecap="round" stroke-linejoin="round"><path stroke="none" d="M0 0h24v24H0z" fill="none"></path><path d="M19.5 13.572l-7.5 7.428l-7.5 -7.428m0 0a5 5 0 1 1 7.5 -6.566a5 5 0 1 1 7.5 6.572"></path></svg>`,
      },
      listMobilitas: [
        {
          id: "integrasi",
          title: "Layanan Terintegrasi",
          text:
            "Dashboard, API, Dan Mobile kami sediakan untuk mengontrol & monitoring lebih mudah.",
        },
        {
          id: "ekspedisi",
          title: "Ekspedisi Terbaik",
          text:
            "Kamu bisa pilih layanan sameday, next day, reguler, ekonomi, kargo dan lainya sesukamu.",
        },
        {
          id: "otomatis",
          title: "Sistem Otomatis",
          text: "Cetak resi / AWB, tracking, saldo COD dan banyak fitur lainnya.",
        },
        {
          id: "alwaysforu",
          title: "Selalu Ada Untukmu",
          text: "Kami selalu ada tanpa libur 24 Jam non stop, dan pihak ekpedisi.",
        },
        {
          id: "actualreport",
          title: "Laporan Aktual",
          text: "Kemudahan pantau paket, pencairan COD, saldo, semuanya.",
        },
        {
          id: "friendly",
          title: "Friendly",
          text: "Ciptakan solusi terbaik dengan masukan, kritik, dan diskusi.",
        },
      ],
    };
  },
};
</script>
