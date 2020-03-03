<template>
    <section
        class="testimonial section center-content"
        :class="[
            hasBgColor && 'has-bg-color',
            invertColor && 'invert-color'
        ]">
        <div class="container-xs">
            <div
                class="testimonial-inner section-inner"
                :class="[
                    topDivider && 'has-top-divider',
                    bottomDivider && 'has-bottom-divider'
                ]">
                <c-section-header :data="sectionHeader" class="center-content" />
                <c-carousel
                    class="tiles-wrap reveal-scale-up"
                    :class="[
                        pushLeft && 'push-left',
                    ]"
                    autorotate
                    :autorotate-timing="7000">
                    <c-carousel-item class="tiles-item">
                        <div class="tiles-item-inner">
                            <div class="testimonial-item-header mb-16">
                                <div class="testimonial-item-image">
                                    <c-image
                                        :src="require('@/assets/images/testimonial-image-01.png')"
                                        alt="Testimonial 01"
                                        :width="56"
                                        :height="56" />
                                </div>
                            </div>
                            <div class="testimonial-item-content">
                                <p class="m-0">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Excepteur sint occaecat cupidatat non proident.
                                </p>
                            </div>
                        </div>
                    </c-carousel-item>

                    <c-carousel-item class="tiles-item">
                        <div class="tiles-item-inner">
                            <div class="testimonial-item-header mb-16">
                                <div class="testimonial-item-image">
                                    <c-image
                                        :src="require('@/assets/images/testimonial-image-02.png')"
                                        alt="Testimonial 02"
                                        :width="56"
                                        :height="56" />
                                </div>
                            </div>
                            <div class="testimonial-item-content">
                                <p class="m-0">
                                    Excepteur sint occaecat cupidatat non proident. Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                                </p>
                            </div>
                        </div>
                    </c-carousel-item>

                    <c-carousel-item class="tiles-item">
                        <div class="tiles-item-inner">
                            <div class="testimonial-item-header mb-16">
                                <div class="testimonial-item-image">
                                    <c-image
                                        :src="require('@/assets/images/testimonial-image-03.png')"
                                        alt="Testimonial 03"
                                        :width="56"
                                        :height="56" />
                                </div>
                            </div>
                            <div class="testimonial-item-content">
                                <p class="m-0">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Excepteur sint occaecat cupidatat non proident.
                                </p>
                            </div>
                        </div>
                    </c-carousel-item>
                </c-carousel>
            </div>
        </div>
    </section>
</template>

<script>
import { SectionTilesProps } from '@/utils/SectionProps.js'
import CSectionHeader from '@/components/sections/partials/SectionHeader.vue'
import CCarousel from '@/components/elements/Carousel.vue'
import CCarouselItem from '@/components/elements/CarouselItem.vue'
import CImage from '@/components/elements/Image.vue'

export default {
  name: 'CTestimonialCarusel',
  components: {
    CSectionHeader,
    CCarousel,
    CCarouselItem,
    CImage
  },
  mixins: [SectionTilesProps],
  data() {
    return {
      sectionHeader: {
        title: '',
        paragraph: ''
      }
    }
  }
}
</script>