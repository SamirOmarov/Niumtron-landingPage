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
                                Advanced Sensor Coverage
                            </h3>
                            <p class="m-0">
                          A radar sensor is usually at the core of the adaptive cruise control (ACC). Installed at the front of the vehicle, the system permanently monitors the road ahead. As long as the road ahead is clear, ACC maintains the speed set by the driver. If the system spots a slower vehicle within its detection range, it gently reduces speed by releasing the accelerator or actively engaging the brake control system. If the vehicle ahead speeds up or changes lanes, the ACC automatically accelerates to the driver’s desired speed.  
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
                            <div style="position:absolute;width:117.8%;max-width:117.8%;top:-4.9%;left:-5.87%;">
                                <c-image
                                    :src="require('@/assets/images/sensors.jpg')"
                                    alt="Features split top 01"
                                    :width="622"
                                    :height="320" />
                            </div>
                        </div>
                    </div>

                    <div class="split-item">
                        <div class="split-item-content center-content-mobile reveal-from-right" data-reveal-container=".split-item">
                            <h3 class="mt-0 mb-12 mr-5">
                                    Lane Assist
                            </h3>
                            <p class="m-0">
                             Even just a momentary lapse in concentration can cause the driver to unintentionally stray from the lane. The lane departure warning function warns the driver of straying from the marked lane and thereby helps to avoid accidents. 
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
                            <div style="position:absolute;width:117.8%;max-width:117.8%;top:0.9%;left:-8.87%;">
                                <c-image
                                    :src="require('@/assets/images/autopilot.jpg')"
                                    alt="Features split top 02"
                                    :width="333"
                                    :height="333" />
                            </div>
                        </div>
                    </div>

                    <div class="split-item">
                        <div class="split-item-content center-content-mobile reveal-from-left" data-reveal-container=".split-item">
                            <h3 class="mt-0 mb-12">
                                System Components
                            </h3>
                            <p class="m-0">
                           Our system consists of following components:
                            </p>
                        </div>
                        <div
                            class="split-item-image mb-12 illustration-element-05 reveal-from-right" data-reveal-container=".split-item"
                            :class="imageFill && 'split-item-image-fill'">
                            <c-image
                                :src="require('@/assets/images/features-split-image.svg')"
                                alt="Features split image 03"
                                :width="528"
                                :height="396" />
                            <div style="position:absolute;width:117.8%;max-width:117.8%;top:-13.9%;left:-9.87%;">
                                <c-image
                                    :src="require('@/assets/images/table.png')"
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
        paragraph: 'System enhances driving comfort by taking over monotonous and tedious driving tasks from drivers '
      }
    }
  }
}
</script>
