<template>
  <nav id="navbar" class="fixed w-full bg-white">
    <div class="flex px-28 py-5 justify-between items-center">
      <div>
        <img
          src="https://kiriminaja.com/assets/atrust/svg-logo-primary.svg"
          class="w-1/4"
          alt=""
        />
      </div>
      <div class="flex gap-6">
        <div v-for="menu in listMenu">
          <router-link :to="menu.path">
            <p class="font-bold hover:text-blue-900">
              {{ menu.name }}
            </p>
          </router-link>
        </div>
      </div>
    </div>
  </nav>
</template>
<script>

export default {
  data () {
    return {
      listMenu:[
        {
          name: "Beranda",
          path: "/",
        },
        {
          name: "Integrasi Api",
          path: "/integrasi-api",
        },
        {
          name: "About",
          path: "/about",
        },
      ]
    }
  }
}
</script>
