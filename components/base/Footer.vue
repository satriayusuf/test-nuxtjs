<template>
  <div class="px-28 py-20 flex justify-center lg:block">
    <div class="lg:flex gap-6 lg:text-left text-center">
      <div class="w-full lg:w-4/6">
        <div class="flex justify-center lg:block">
          <div>

          <img
            src="https://kiriminaja.com/assets/atrust/svg-logo-primary.svg"
            class="w-1/5"
            alt=""
          />
          </div>
        </div>
        <div class="w-full lg:w-1/2">
          <p class="text-gray-400 font-semibold mt-3">PT. Selalu Siap Solusi</p>
          <p class="mt-3 text-gray-800">{{ contact.location }}</p>
          <p class="mt-3 text-gray-800">{{ contact.email }}</p>
          <p class="mt-3 text-gray-800">{{ contact.phone }}</p>
        </div>
      </div>
      <div class="w-full lg:w-1/4">
        <div>
          <p class="text-gray-400 font-semibold mt-3">Tautan Cepat</p>
        </div>
        <div v-for="content in shortcutLink">
          <a class="text-gray-800 hover:opacity-75" :href="content.link" target="_blank">
            <p class="mt-5">
              {{ content.text }}
            </p>
          </a>
        </div>
      </div>
      <div class="w-full lg:w-1/4">
        <div>
          <p class="text-gray-400 font-semibold mt-3">KiriminAja</p>
        </div>
         <div v-for="content in about">
          <a class="text-gray-800 hover:opacity-75" :href="content.link" target="_blank">
            <p class="mt-5">
              {{ content.text }}
            </p>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      contact: {
        location:
          "Jl. Palagan Tentara Pelajar No. 30 KM 08, Mudal, Kelurahan Sariharjo, Kecamatan Ngaglik, Kabupaten Sleman, Provinsi Daerah Istimewa Yogyakarta",
        email: "support@kiriminaja.com",
        phone: "0274 8000 123",
      },
      shortcutLink: [
        {
          text: "Cek Tarif Aja",
          link: "https://kiriminaja.com/cekaja",
        },
        {
          text: "Kabar Buatmu",
          link: "https://kiriminaja.com/kabar",
        },
        {
          text: "Manajemen Order",
          link: "https://kiriminaja.com/praktisin",
        },
        {
          text: "Integrasi API",
          link: "https://kiriminaja.com/api-integration",
        },
        {
          text: "Karir",
          link: "https://kiriminaja.com/careers",
        },
      ],
      about: [
        {
          text: 'Tentang Kami',
          link: 'https://kiriminaja.com/about'
        },
        {
          text: 'Syarat & Ketentuan',
          link: 'https://kiriminaja.com/syarat-ketentuan'
        },
        {
          text: 'Kebijakan Privasi',
          link: 'https://kiriminaja.com/privacy-policy'
        },
        {
          text: 'Fakta & Pertanyaan',
          link: 'https://kiriminaja.com/faq'
        }
      ]
    };
  },
};
</script>
