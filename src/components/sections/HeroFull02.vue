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
                    <div class="container-xs">
                        <h1 class="mt-0 reveal-from-top">
                            Engage Your Visitors with a beautiful template
                        </h1>
                    </div>
                </div>
                <div class="hero-figure illustration-element-02 reveal-from-bottom" data-reveal-delay="200">
                    <a
                        data-video="https://player.vimeo.com/video/174002812"
                        href="#"
                        aria-controls="video-modal"
                        @click.prevent="videoModalActive = true">
                        <c-image
                            :src="require('@/assets/images/video-placeholder.png')"
                            alt="Video"
                            :width="896"
                            :height="504" />
                    </a>
                </div>
                <c-modal
                    id="video-modal"
                    :active.sync="videoModalActive"
                    video="https://player.vimeo.com/video/174002812"
                    video-tag="iframe" />
            </div>
        </div>
    </section>
</template>

<script>
import { SectionProps } from '@/utils/SectionProps.js'
import CImage from '@/components/elements/Image.vue'
import CModal from '@/components/elements/Modal.vue'

export default {
  name: 'CHeroFull',
  mixins: [SectionProps],
  components: {
    CImage,
    CModal
  },
  data() {
    return {
      videoModalActive: false
    }
  }
}
</script>