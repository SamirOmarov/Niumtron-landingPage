<template>
    <section
        class="pricing section"
        :class="[
            hasBgColor && 'has-bg-color',
            invertColor && 'invert-color'
        ]">
        <div class="container">
            <div
                class="pricing-inner section-inner pb-0"
                :class="[
                    topDivider && 'has-top-divider',
                    bottomDivider && 'has-bottom-divider'
                ]">
                <c-section-header :data="sectionHeader" class="center-content" />
                <c-pricing-switcher
                    v-if="pricingSwitcher"
                    :state.sync="pricingSwitchOn"
                    :labels="pricingSwitchLabels" />
                <div
                    class="tiles-wrap illustration-section-08"
                    :class="[
                        pushLeft && 'push-left',
                    ]">
                    <div class="tiles-item reveal-rotate-from-left" data-reveal-delay="100">
                        <div class="tiles-item-inner">
                            <div class="pricing-item-content">
                                <div class="pricing-item-header pb-24 mb-24">
                                    <div class="pricing-item-price mb-4">
                                        <span class="pricing-item-price-currency h2">$</span>
                                        <span class="pricing-item-price-amount h1">{{pricingSwitchOn ? '44' : '55'}}</span>
                                    </div>
                                    <div class="text-xs">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                                    </div>
                                </div>
                                <div class="pricing-item-features mb-40">
                                    <div class="pricing-item-features-title h6 text-xs text-color-high mb-24">
                                        What’s included
                                    </div>
                                    <ul class="pricing-item-features-list list-reset text-xs mb-32">
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li>Excepteur sint occaecat velit</li>
                                        <li>Excepteur sint occaecat velit</li>
                                    </ul>
                                </div>
                            </div>
                            <div class="pricing-item-cta mb-8">
                                <c-button tag="a" color="primary" wide href="#">Start free trial</c-button>
                            </div>
                        </div>
                    </div>

                    <div class="tiles-item reveal-scale-down">
                        <div class="tiles-item-inner">
                            <div class="pricing-item-content">
                                <div class="pricing-item-header pb-24 mb-24">
                                    <div class="pricing-item-price mb-4">
                                        <span class="pricing-item-price-currency h2">$</span>
                                        <span class="pricing-item-price-amount h1">{{pricingSwitchOn ? '74' : '85'}}</span>
                                    </div>
                                    <div class="text-xs">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                                    </div>
                                </div>
                                <div class="pricing-item-features mb-40">
                                    <div class="pricing-item-features-title h6 text-xs text-color-high mb-24">
                                        What’s included
                                    </div>
                                    <ul class="pricing-item-features-list list-reset text-xs mb-32">
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li>Excepteur sint occaecat velit</li>
                                    </ul>
                                </div>
                            </div>
                            <div class="pricing-item-cta mb-8">
                                <c-button tag="a" color="primary" wide href="#">Start free trial</c-button>
                            </div>
                        </div>
                    </div>

                    <div class="tiles-item reveal-rotate-from-right" data-reveal-delay="100">
                        <div class="tiles-item-inner">
                            <div class="pricing-item-content">
                                <div class="pricing-item-header pb-24 mb-24">
                                    <div class="pricing-item-price mb-4">
                                        <span class="pricing-item-price-currency h2">$</span>
                                        <span class="pricing-item-price-amount h1">{{pricingSwitchOn ? '94' : '105'}}</span>
                                    </div>
                                    <div class="text-xs">
                                        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.
                                    </div>
                                </div>
                                <div class="pricing-item-features mb-40">
                                    <div class="pricing-item-features-title h6 text-xs text-color-high mb-24">
                                        What’s included
                                    </div>
                                    <ul class="pricing-item-features-list list-reset text-xs mb-32">
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                        <li class="is-checked">Excepteur sint occaecat velit</li>
                                    </ul>
                                </div>
                            </div>
                            <div class="pricing-item-cta mb-8">
                                <c-button tag="a" color="primary" wide href="#">Start free trial</c-button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { SectionTilesProps } from '@/utils/SectionProps.js'
import CSectionHeader from '@/components/sections/partials/SectionHeader.vue'
import CPricingSwitcher from '@/components/sections/partials/PricingSwitcher.vue'
import CButton from '@/components/elements/Button.vue'

export default {
  name: 'CPricing',
  components: {
    CSectionHeader,
    CPricingSwitcher,
    CButton
  },
  mixins: [SectionTilesProps],
  props: {
    pricingSwitcher: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      sectionHeader: {
        title: 'Storm template pricing',
        paragraph:
          'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore aliqua.'
      },
      pricingSwitchLabels: {
        type: 'Billing Period', // screen-reader text
        default: 'Billed Monthly',
        switchOn: 'Billed Annually'
      },
      pricingSwitchOn: true
    }
  }
}
</script>