<template>
    <fragment>
        <c-hero-full class="illustration-section-01" />
        <c-features-tiles class="illustration-section-02" />
        <c-features-split invert-mobile top-divider image-fill />
        <c-pricing top-divider pricing-switcher />
        <c-testimonial class="illustration-section-07" />
    </fragment>
</template>

<script>
// import layout
import CLayout from '@/layouts/LayoutDefault.vue'
// import CLayout from '@/layouts/LayoutAlternative.vue'

// import sections
import CHeroFull from '@/components/sections/HeroFull.vue'
import CFeaturesTiles from '@/components/sections/FeaturesTiles.vue'
import CFeaturesSplit from '@/components/sections/FeaturesSplit.vue'
// import CPricing from '@/components/sections/Pricing.vue'
import CTestimonial from '@/components/sections/TestimonialCarousel.vue'

export default {
  name: 'Home',
  components: {
    CHeroFull,
    CFeaturesTiles,
    CFeaturesSplit,
    // CPricing,
    CTestimonial
  },
  created() {
    this.$emit('update:layout', CLayout)
  }
}
</script>
