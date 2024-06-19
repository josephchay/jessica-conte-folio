<template>
  <div class="c-archive">
    <svg class="cursor" width="32" ref="cursor" height="32" viewBox="0 0 20 20">
      <circle class="cursor__inner" cx="10" cy="10" r="5" />
    </svg>
    <div class="c-archive__header">
      <nuxt-link to="/profile">
        <animated-link class="c-bezier">
          Profile
        </animated-link>
      </nuxt-link>
      <nuxt-link to="/">
        <animated-link class="c-bezier">
          Close
        </animated-link>
      </nuxt-link>
    </div>
    <LocomotiveScroll
      ref="scroller"
      class="horizontal"
      :getted-options="{
        direction: 'horizontal',
        smooth: true,
        getSpeed: true,
        lerp: 0.08
        // Other options
      }"
    >
      <div class="c-archive__main">
        <div>
          <div class="archive__intro">
            <p>
              This archive contains video clips, art and pictures related to
              Jess and her work, respective owners of each piece of work have
              been credited. Contact us for content removal
            </p>

            <button class="credits-link show-mobile" @click="openModal">
              <div class="c-inner">
                <animated-link class="c-bezier">
                  credits
                </animated-link>
              </div>
            </button>

            <h1>
              “Each day you must choose the pain of discipline or the pain of regret."
            </h1>
            <nuxt-link to="/" class="home-link">
              <animated-link class="c-bezier">
                Go to Home
              </animated-link>
            </nuxt-link>

            <button class="credits-link show-desktop" @click="openModal">
              <div class="c-inner">
                <animated-link class="c-bezier">
                  credits
                </animated-link>
              </div>
            </button>
          </div>
          <div class="archive__images">
            <div class="c-image sm">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645095/1_qbqcak.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645130/2_ffm8ol.jpg);
                "
                />
              </div>

              <div class="c-image sm nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645138/4_ppy1xp.jpg);
                "
                />
              </div>

              <div class="c-image md nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645142/5_g8nldj.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645145/6_vnnvog.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645151/7_klieef.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645167/10_a6qtoz.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645163/9_mqpaxl.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718808823/32_bhqxx8.jpg);
                "
                />
              </div>

              <div class="c-image md nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645158/8_ngbznh.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645531/12_clfacj.webp);
                "
                />
              </div>

              <div class="c-image md nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645391/11_qtr3lm.jpg);
                "
                />
              </div>

              <div class="c-image sm nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645694/13_dzjxv7.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645735/14_z7te6p.jpg);
                "
                />
              </div>

              <div class="c-image sm nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718645878/15_gplq2g.webp);
                "
                />
              </div>

              <div class="c-image sm nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651067/16_anekts.jpg);
                "
                />
              </div>

              <div class="c-image sm">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651195/17_wmnznj.jpg);
                "
                />
              </div>

              <div class="c-image md">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651257/18_gbdz5b.jpg);
                "
                />
              </div>

              <div class="c-image sm nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651672/22_kplots.jpg);
                "
                />
              </div>

              <div class="c-image xs nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651275/19_nai7wj.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651642/21_iqwvwa.jpg); // TODO HELLP
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                    background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718557539/profile_gz2mqx.jpg);
                  "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651908/23_m4ez3h.jpg);
                "
                />
              </div>

              <!-- Copy Image -->

              <div class="c-image md">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651914/24_av4qvx.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651920/25_skafmx.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718651937/26_ontsvw.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718652003/27_tode87.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718652052/28_vmtz9f.jpg);
                "
                />
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718652107/30_cspxok.jpg);
                "
                />
              </div>

              <div class="c-image md nobp">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718652114/31_kloodf.jpg);
                "
                />
              </div>

              <div class="c-circle">
                <div class="c-circle__inner">
                  <div class="heading">
                    <h3>
                      the <br />
                      End
                    </h3>
                  </div>

                  <nuxt-link to="/" class="home-link">
                    <animated-link class="c-bezier"> Go to Home </animated-link>
                  </nuxt-link>
                </div>
              </div>

              <div class="c-image xs">
                <div
                  data-scroll
                  data-scroll-speed="-0.8"
                  class="bg-image"
                  style="
                  background-image: url(https://res.cloudinary.com/di3otod6k/image/upload/v1718652209/32_jdrsil.avif);
                "
                />
              </div>
          </div>
        </div>
      </div>
    </LocomotiveScroll>
  </div>
</template>

<script>

import AnimatedArrow from "@/components/AnimatedArrow.vue";
import AnimatedLink from "@/components/AnimatedLink/AnimatedLink.vue";
import { map, clamp } from "@/utils/index";
import gsap from "gsap/all";
import { Cursor } from "~/animations/cursor";

export default {
  components: { AnimatedArrow, AnimatedLink },

  /**
   * TODO: outsource the exit animations into one and reuse
   */
  transition: {
    name: "profile",
    mode: "out-in",
    css: false,
    appear: true,
    beforeEnter(el) {
      gsap.set(el, {
        opacity: 0
      });
    },
    enter(el, done) {
      const tl = gsap.timeline({
        onComplete: done
      });
      tl.to(el, {
        opacity: 1,
        duration: 1.5
      })
        .set(".archive__images .c-image", { autoAlpha: 1 }, "-=1.5")
        .from(
          ".archive__images .c-image",
          {
            duration: 1.5,
            yPercent: 100,
            ease: "Expo.easeInOut"
          },
          "-=1.5"
        )
        .from(".archive__images .bg-image", {
          duration: 1.5,
          yPercent: -100,
          delay: -1.5,
          ease: "Expo.easeInOut"
        })
        .from(".archive__images .bg-image", {
          duration: 1.5,
          scale: 1.2,
          delay: -1.4,
          ease: "Expo.easeInOut"
        });
    },
    beforeLeave(el) {
      gsap.set(".c-exit", {
        zIndex: 30,
        top: "unset",
        bottom: 0
      });
      gsap.set(".exit-span", {
        opacity: 1
      });
    },
    leave(el, done) {
      const tl = gsap.timeline({
        onComplete: done
      });

      tl.to(".c-exit", {
        height: window.innerHeight,
        duration: 1.5,
        ease: "Expo.easeInOut"
      })
        .set(".c-exit", {
          top: 0,
          bottom: "unset"
        })
        .from(
          ".exit-span",
          {
            yPercent: 100,
            duration: 1,
            skewY: 5,
            stagger: {
              amount: 0.1
            },
            ease: "power2.out"
          },
          "-=.5"
        )
        .set(el, {
          opacity: 0
        })
        .to(".exit-span", {
          opacity: 0,
          duration: 1,
          ease: "power2.out"
        })
        .to(
          ".c-exit",
          {
            height: 0,
            duration: 1.5,
            ease: "Expo.easeInOut"
          },
          "-=1"
        );
    }
  },
  mounted() {
    const locomotive = this.$refs.scroller.locomotive;
    this.$nuxt.$emit("update-locomotive");
    this.beginCursor();

    let direction = "horizontal";
    window.addEventListener("resize", () => {
      const width = window.innerWidth;

      if (width <= 768 && direction !== "vertical") {
        locomotive.destroy();
        locomotive.init();
        direction = "vertical";
      }

      if (width > 768 && direction === "vertical") {
        locomotive.destroy();
        locomotive.init();
        direction = "horizontal";
      }
    });

    let scroll = { cache: 0, current: 0 };
    const allImgs = [...document.querySelectorAll(".archive__images .c-image")];
    locomotive.on("scroll", obj => {
      scroll.current = obj.scroll.x;
      const distance = scroll.current - scroll.cache;
      scroll.cache = scroll.current;
      const skewVal = map(distance, -50, 50, -15, 15);
      allImgs.forEach(
        el => (el.style.transform = `skewX(${clamp(skewVal, -1, 1)}deg)`)
      );
    });
    locomotive.update();
  },
  methods: {
    openModal() {
      this.$store.commit("updateModal", true);
    },
    beginCursor() {
      const cursorRef = this.$refs.cursor;
      const cursor = new Cursor(cursorRef);
      [...document.querySelectorAll("a")].forEach(link => {
        link.addEventListener("mouseenter", () => cursor.enter());
        link.addEventListener("mouseleave", () => cursor.leave());
      });
      [...document.querySelectorAll("button")].forEach(link => {
        link.addEventListener("mouseenter", () => cursor.enter());
        link.addEventListener("mouseleave", () => cursor.leave());
      });
    }
  }
};
</script>

<style lang="scss" scoped></style>
