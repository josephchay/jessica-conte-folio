<template>
  <div class="desktop-landing">
    <div class="c-landing__header">
      <nuxt-link to="/profile">
        <AnimatedLink class="c-bezier">
          Profile
        </AnimatedLink>
      </nuxt-link>
      <nuxt-link to="/archive">
        <AnimatedLink class="c-bezier">
          Archive
        </AnimatedLink>
      </nuxt-link>
    </div>
    <div class="c-landing__desktop">
      <div class="hero-content">
        <div class="hero-image">
          <div class="image-mask"></div>
          <div class="c-image"></div>
        </div>
        <div class="c-name__image">
          <div class="inner" />
        </div>
        <div class="c-name__details">
          <h1 class="details-title span-overflow">
            <span class="ov-inner">
              jess_conte
            </span>
          </h1>
          <p class="details-jd span-overflow">
            <span class="ov-inner">
              MODEL & <br />
              YOUTUBER
            </span>
          </p>
        </div>

        <button class="credits-link" @click="openModal">
          <div class="c-inner">
            <AnimatedLink class="c-bezier">
              credits
            </AnimatedLink>
          </div>
        </button>
      </div>
      <div class="hero-links">
        <div class="c-hoverlink hover-link-1">
          <div class="span-overflow">
            <div class="ov-inner">
              <p>
                Based in United States. Jess runs a youtube channel where she
                posts -
              </p>
            </div>
          </div>
          <div>
            <hover-link
              label="VLOGS + ARTS"
              assetUrl="https://res.cloudinary.com/di3otod6k/video/upload/v1718530413/vlogs_arts_thumnail_vid_p2xuwu.mp4"
              href="https://www.youtube.com/@JessConte"
            >
              <sup class="c-hoverlink__super">01</sup>
              <div class="link-overflow">
                <span class="ov-inner">
                  <AnimatedLink>
                    VL<span class="fraunces">O</span>GS
                    <span class="fraunces">+</span> ARTS
                  </AnimatedLink>
                </span>
              </div>
            </hover-link>
          </div>
        </div>

        <div class="c-hoverlink hover-link-2">
          <div>
            <hover-link
              label="Video Mashups"
              assetUrl="https://res.cloudinary.com/di3otod6k/video/upload/v1718544704/video_mashups_igthumgnail_vid_jfmfjz.mp4"
              href="https://www.instagram.com/jess/"
            >
              <sup class="c-hoverlink__super">02</sup>
              <div class="link-overflow">
                <span class="ov-inner">
                  <AnimatedLink>
                    VIDE<span class="fraunces">O</span> MASHUPS
                  </AnimatedLink>
                </span>
              </div>
            </hover-link>
          </div>
          <div class="span-overflow">
            <span class="ov-inner">
              <p>
                these mostly go on instagram to her 2.1M plus audience. 🔥 edits,
                we highly recommend.
              </p>
            </span>
          </div>
        </div>
        <div class="c-hoverlink hover-link-3">
          <div class="image-details">
            <div class="span-overflow">
              <span class="ov-inner">
                <p>
                  She has collaborated with multiple fashion brands.
                </p>
              </span>
            </div>
            <div class="c-image c-model__image ov-h">
              <img
                src="https://res.cloudinary.com/di3otod6k/image/upload/v1718557920/modelling_aolqc9.jpg"
                alt=""
              />
            </div>
          </div>
          <div>
            <hover-link
              label="Modelling"
              assetUrl="https://res.cloudinary.com/di3otod6k/video/upload/v1718556645/modelling_thumbnail_vid_c6cssf.mp4"
              href="https://www.instagram.com/jess/"
            >
              <sup class="c-hoverlink__super">03</sup>
              <div class="link-overflow">
                <span class="ov-inner">
                  <AnimatedLink>
                    M<span class="fraunces">O</span>DELLING
                  </AnimatedLink>
                </span>
              </div>
            </hover-link>
          </div>
        </div>
        <nuxt-link class="c-circular-link" to="/profile">
          <circular-link>
            View Jess's Profile
          </circular-link>
        </nuxt-link>
      </div>
    </div>
  </div>
</template>

<script>

import CircularLink from "../CircularLink/CircularLink.vue";
import HoverLink from "../HoverLink/HoverLink.vue";

export default {
  components: { CircularLink, HoverLink },
  methods: {
    openModal() {
      this.$store.commit("updateModal", true);
    }
  }
};
</script>

<style lang="scss" scoped></style>
