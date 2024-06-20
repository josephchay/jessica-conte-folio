<template>
  <transition
    @before-enter="beforeEnter"
    @enter="enter"
    :css="false"
    @before-leave="beforeLeave"
    @leave="leave"
  >
    <div class="c-modal" v-if="modalOpen">
      <div class="c-modal__main" ref="main">
        <button to="/" class="home-link" @click="closeModal">
          <animated-link class="c-bezier">
            CLOSE
          </animated-link>
        </button>

        <div class="main__top sect">
          <div class="left">
            <h1>
              WHO MADE THIS SITE?
            </h1>
              <p>
                <a
                  href="https://josephchay.netlify.app/"
                  target="__blank"
                  style="text-decoration: underline;"
                  >
                    Joseph
                  </a
                >
                - Development 2024 Build
              </p>
            <p>
              <a
                href="https://josephchay.netlify.app/"
                target="__blank"
                style="text-decoration: underline;"
                >
                  Joseph
                </a
              >
              - Art Direction
            </p>
            <p>
              <a
                href="https://josephchay.netlify.app/"
                target="__blank"
                style="text-decoration: underline;"
                >
                  Joseph
                </a
              >
              - UI Design
            </p>
            <p>
              <a
                href="https://josephchay.netlify.app/"
                target="__blank"
                style="text-decoration: underline;"
                >
                  Joseph
                </a
              >
              - Motion & Interaction Design
            </p>
          </div>
          <div class="right">
            <img
              src="https://res.cloudinary.com/di3otod6k/image/upload/v1718561909/desk-setup_xz1h6d.avif"
              alt=""
            />
          </div>
        </div>
        <div class="main__bottom sect">
          <div class="left">
            <h1>
              TYPESETTING
            </h1>
            <p>
              Type for this website was set in Fraunces and HK Grotesk
            </p>
            <div class="left-footer">
              <p>A folio for Jessica Conte</p>
              <p>© 2024</p>
            </div>
          </div>
          <div class="right">
            <h1>WE USED WORKS FROM:</h1>
            <p>
              Youtube Channel - Jess Conte, Instagram - Jess Conte.
            </p>
            <a href="mailto:codebulous@gmail.com">
              Request content removal
            </a>
          </div>
        </div>

        <div class="main__footer">
          <p>A folio for Jessica Conte</p>
          <p>© 2024</p>
        </div>
      </div>
    </div>
  </transition>
</template>

<script>

import gsap from "gsap/all";
import { mapState, mapGetters } from "vuex";
import AnimatedLink from "../AnimatedLink/AnimatedLink.vue";
export default {
  components: { AnimatedLink },

  computed: {
    ...mapState(["modalOpen", "imagesLoaded"])
  },
  methods: {
    closeModal() {
      this.$store.commit("updateModal", false);
    },
    beforeEnter(el) {
      gsap.set(el, {
        height: 0,
        bottom: 0
      });
    },

    enter(el, done) {
      const timeline = gsap.timeline({
        onComplete() {
          done();
        }
      });
      timeline
        .to(el, {
          height: "100vh",
          duration: 0.8,
          ease: "power2.inOut"
        })
        .set(el, { top: 0 })
        .from(".c-modal__main", {
          opacity: 0
        });
    },
    beforeLeave(el) {
      gsap.set(el, {
        top: 0,
        bottom: "unset"
      });
    },

    leave(el, done) {
      const timeline = gsap.timeline({
        onComplete: done
      });
      timeline.to(el, {
        height: 0,
        duration: 0.8,
        ease: "power2.inOut"
      });
    }
  }
};
</script>

<style lang="scss" scoped></style>
