<template>
    <fragment>
        <c-header navPosition="right" class="reveal-from-bottom" />
        <main class="site-content">
            <slot />
        </main>
        <c-footer topDivider class="illustration-section-09" />
    </fragment>
</template>

<script>
import CHeader from '@/components/layout/Header.vue'
import CFooter from '@/components/layout/Footer.vue'
export default {
  components: {
    CHeader,
    CFooter
  }
}
</script>