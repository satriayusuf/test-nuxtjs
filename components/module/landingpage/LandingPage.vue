<template>
  <div>
    <div class="pt-28 lg:px-28 px-12">
      <section id="carrousel">
        <module-landingpage-children-carrousel />
      </section>
      <section id="form-simulasi" class="mt-20">
        <module-landingpage-children-formSimulation />
      </section>
      <!-- <section id="list-courier" class="mt-20">
      <module-landingpage-children-listCourier />
    </section> -->
      <section id="mobilitas" class="mt-20">
        <module-landingpage-children-mobilitas />
      </section>
      <section id="banner" class="mt-20">
        <img
          src="https://kiriminaja.com/assets/home-2/pesta-pora-new.png"
          class="w-full h-auto"
          alt=""
        />
      </section>
      <section id="list-feature" class="mt-20">
        <module-landingpage-children-listFeature />
      </section>
    </div>
    <div>
      <section id="cta" class="mt-20">
        <module-landingpage-children-callToAction />
      </section>
    </div>
  </div>
</template>

<script>
export default {
  methods: {},
};
</script>
