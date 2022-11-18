<template>
  <div class="bg-gradient-to-br from-purple-900 to-blue-900 w-full pt-10 px-10 rounded">
    <div class="flex gap-6">
      <div class="w-2/3">
        <img
          src="https://kiriminaja.com/assets/home-2/call-to-action.png"
          class="w-full h-auto"
          alt=""
        />
      </div>
      <div class="w-full">
        <h1 class="text-white text-5xl font-bold mt-8 capitalize">
          Semua bisa mulai kirim paket tanpa ribet !
        </h1>
        <h2 class="text-white text-lg mt-8">
          Jadikan pengalaman pengiriman paket lebih mudah dengan
          <strong>KiriminAja</strong>.
        </h2>
        <div class="flex mt-10 w-2/3">
          <div>
            <img
              src="https://kiriminaja.com/assets/service/v2/googleplay-compressed.png"
              alt=""
              class="cursor-pointer hover:opacity-80 w-10/12"
            />
          </div>
          <div>
            <img
              src="https://kiriminaja.com/assets/service/v2/appstore-compressed.png"
              alt=""
              class="cursor-pointer hover:opacity-80 w-10/12"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carrousel: [],
      showOneCarrousel: {
        id: "",
        text: "",
        title: "",
        img: "",
      },
    };
  },
  async mounted() {
    await this.getDataCarrousel();
    this.setCarrousel();
  },
  watch: {
    watchCarrousel() {
      this.setCarrousel();
    },
  },
  methods: {
    async getDataCarrousel() {
      // ======================================= IF U NEED RES FOR MOCK API
      // const resData = {
      //   data: [
      //     {
      //       id: "1",
      //       title: "November Untung Bener",
      //       text: "cuma kirim paket bisa dapetin sepeda",
      //       img:
      //         "https://kiriminaja.com/storage/Slider/November22/1668074906_slider%20november.png",
      //     },
      //     {
      //       id: "2",
      //       title: "November Bntung Bener",
      //       text: "cuma kirim paket bisa dapetin sepeda",
      //       img:
      //         "https://kiriminaja.com/storage/Slider/November22/1668074906_slider%20november.png",
      //     },
      //   ],
      // };

      try {
        const data = await this.$axios.$get("http://localhost:3001/carrousel"); // mock use mockoon
        this.carrousel = data;
      } catch (err) {
        console.error(err);
      }
    },
    setCarrousel() {
      // let interval;
      // if (this.showOneCarrousel.id) {
      //   interval = setInterval(() => {
      //     this.showOneCarrousel = this.carrousel.find(
      //       (item) => item.id !== this.showOneCarrousel.id
      //     );
      //   }, (5 * 1000) / 100);
      // } else {
      //   this.showOneCarrousel.id = this.carrousel[0].id;
      //   this.showOneCarrousel.text = this.carrousel[0].text;
      //   this.showOneCarrousel.title = this.carrousel[0].title;
      //   console.log(this.showOneCarrousel);
      // }
    },
  },
};
</script>
