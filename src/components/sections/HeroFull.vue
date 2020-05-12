<template>
    <section
        class="hero section center-content"
        :class="[
            hasBgColor && 'has-bg-color',
            invertColor && 'invert-color'
        ]">
        <div class="container-sm">
            <div
                class="hero-inner section-inner"
                :class="[
                    topDivider && 'has-top-divider',
                    bottomDivider && 'has-bottom-divider'
                ]">
                <div class="hero-content">
                    <h1 class="mt-0 mb-16 reveal-from-bottom" data-reveal-delay="200">
                      Future of Driving
                    </h1>
                    <div class="container-xs">
                        <p class="m-0 mb-32 reveal-from-bottom" data-reveal-delay="400">
                            Niumtron is a research and development company that focuses on innovation.
                        </p>
                        <!-- <div class="reveal-from-bottom" data-reveal-delay="600">
                            <c-button tag="a" color="primary" href="https://cruip.com/">
                                Get started
                            </c-button>
                        </div> -->
                    </div>
                </div>
                <div class="hero-figure illustration-element-01 reveal-from-bottom" data-reveal-value="20px" data-reveal-delay="800">
                    <c-image
                        class="has-shadow"
                        :src="require('@/assets/anim.gif')"
                        alt="Hero"
                         />
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { SectionProps } from '@/utils/SectionProps.js'
// import CButton from '@/components/elements/Button.vue'
import CImage from '@/components/elements/Image.vue'

export default {
  name: 'CHeroFull',
  mixins: [SectionProps],
  components: {
    // CButton,
    CImage
  }
}
</script>
