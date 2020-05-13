<template>
    <fragment>
        <!-- <c-hero-full class="illustration-section-01" /> -->
        <c-team class="illustration-section-03" />

    </fragment>
</template>

<script>
// import layout
import CLayout from '@/layouts/LayoutAlternative.vue'
// import section header
// import sections
import CTeam from '@/components/sections/Team.vue'
import CGenericSection from '@/components/sections/GenericSection.vue'
// import some required elements

export default {
  name: 'Secondary',
  components: {
    CTeam,
  },
  data() {
    return {
      genericSection01Header: {
        title: 'FAQ - Lorem ipsum is placeholder text commonly used.'
      },
      genericSection02Header: {
        title: 'Modal - Lorem ipsum is placeholder text commonly used.'
      },      
      genericSection03Header: {
        title: 'Buttons - Lorem ipsum is placeholder text commonly used.'
      },
      genericSection04Header: {
        title: 'Input forms - Lorem ipsum is placeholder text commonly used.'
      },
      demoModalActive: false
    }
  },
  created() {
    this.$emit('update:layout', CLayout)
  }
}
</script>
