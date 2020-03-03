<template>
    <section
        class="features-split section"
        :class="[
            hasBgColor && 'has-bg-color',
            invertColor && 'invert-color'
        ]">
        <div class="container">
            <div
                class="features-split-inner section-inner"
                :class="[
                    topDivider && 'has-top-divider',
                    bottomDivider && 'has-bottom-divider'
                ]">
                <c-section-header :data="sectionHeader" class="center-content" />
                <div
                    class="split-wrap"
                    :class="[
                        invertMobile && 'invert-mobile',
                        invertDesktop && 'invert-desktop'
                    ]">
                    <div class="split-item">
                        <div class="split-item-content center-content-mobile reveal-from-left" data-reveal-container=".split-item">
                            <h3 class="mt-0 mb-12">
                                Advanced features
                            </h3>
                            <p class="m-0">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Excepteur sint occaecat cupidatat non proident.
                            </p>
                        </div>
                        <div
                            class="split-item-image illustration-element-03 reveal-from-right" data-reveal-container=".split-item"
                            :class="imageFill && 'split-item-image-fill'">
                            <c-image
                                :src="require('@/assets/images/features-split-image.svg')"
                                alt="Features split image 01"
                                :width="528"
                                :height="396" />
                            <div style="position:absolute;width:117.8%;max-width:117.8%;top:-9.9%;left:-5.87%;">
                                <c-image
                                    :src="require('@/assets/images/features-split-top-01.png')"
                                    alt="Features split top 01"
                                    :width="622"
                                    :height="510" />
                            </div>
                        </div>
                    </div>

                    <div class="split-item">
                        <div class="split-item-content center-content-mobile reveal-from-right" data-reveal-container=".split-item">
                            <h3 class="mt-0 mb-12">
                                Advanced features
                            </h3>
                            <p class="m-0">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Excepteur sint occaecat cupidatat non proident.
                            </p>
                        </div>
                        <div
                            class="split-item-image illustration-element-04 reveal-from-left" data-reveal-container=".split-item"
                            :class="imageFill && 'split-item-image-fill'">
                            <c-image
                                :src="require('@/assets/images/features-split-image.svg')"
                                alt="Features split image 02"
                                :width="528"
                                :height="396" />
                            <div style="position:absolute;width:117.8%;max-width:117.8%;top:-9.9%;left:-5.87%;">
                                <c-image
                                    :src="require('@/assets/images/features-split-top-02.png')"
                                    alt="Features split top 02"
                                    :width="622"
                                    :height="510" />
                            </div>
                        </div>
                    </div>

                    <div class="split-item">
                        <div class="split-item-content center-content-mobile reveal-from-left" data-reveal-container=".split-item">
                            <h3 class="mt-0 mb-12">
                                Advanced features
                            </h3>
                            <p class="m-0">
                                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Excepteur sint occaecat cupidatat non proident.
                            </p>
                        </div>
                        <div
                            class="split-item-image illustration-element-05 reveal-from-right" data-reveal-container=".split-item"
                            :class="imageFill && 'split-item-image-fill'">
                            <c-image
                                :src="require('@/assets/images/features-split-image.svg')"
                                alt="Features split image 03"
                                :width="528"
                                :height="396" />
                            <div style="position:absolute;width:117.8%;max-width:117.8%;top:-9.9%;left:-5.87%;">
                                <c-image
                                    :src="require('@/assets/images/features-split-top-03.png')"
                                    alt="Features split top 03"
                                    :width="622"
                                    :height="510" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { SectionSplitProps } from '@/utils/SectionProps.js'
import CSectionHeader from '@/components/sections/partials/SectionHeader.vue'
import CImage from '@/components/elements/Image.vue'

export default {
  name: 'CFeaturesSplit',
  components: {
    CSectionHeader,
    CImage
  },
  mixins: [SectionSplitProps],
  data() {
    return {
      sectionHeader: {
        title: 'The complex made simple',
        paragraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore aliqua.'
      }
    }
  }
}
</script>