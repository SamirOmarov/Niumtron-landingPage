<template>
    <section
        class="cta section center-content"
        :class="[
            hasBgColor && 'has-bg-color',
            invertColor && 'invert-color'
        ]">
        <div class="container">
            <div
                class="cta-inner section-inner"
                :class="[
                    topDivider && 'has-top-divider',
                    bottomDivider && 'has-bottom-divider',
                    split && 'cta-split'
                ]">
                <div class="container-xs">
                    <div class="cta-slogan reveal-from-top">
                        <h2 class="mt-0 mb-16">
                            Ready to get started?
                        </h2>
                        <p class="m-0">
                            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore aliqua.
                        </p>
                    </div>
                    <div class="cta-action reveal-scale-up" data-reveal-delay="200">
                        <c-button tag="a" color="primary" wide-mobile href="#">
                            Start free trial
                        </c-button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { SectionProps } from '@/utils/SectionProps.js'
import CButton from '@/components/elements/Button.vue'

export default {
  name: 'CCta',
  components: {
    CButton
  },
  mixins: [SectionProps],
  props: {
    split: {
      type: Boolean,
      default: false
    }
  }
}
</script>