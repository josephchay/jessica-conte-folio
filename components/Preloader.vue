<template>
  <div class="c-preloader" ref="preloader">
    <div class="c-preloader__inner">
      <!-- <button @click="closeLoader">Close</button> -->
      <div>
        <div class="percentages__container">
          <h1 class="fraunces heading-1">
            <span class="percentages">
              <div class="mark">
                ‘
              </div>
              <div class="fake-zero">0</div>
              <span class="p-inner">
                <span class="hide-first">000</span>
                <span
                  v-for="(percentage, index) in numbersArr"
                  :class="
                    `subsequent ${
                      index + 1 < numbersArr.length ? 'hide-first' : ''
                    }`
                  "
                  :key="index"
                  :style="`top: ${(index + 1) * 100}%`"
                >
                  {{ percentage }}
                </span>
              </span>
            </span>
          </h1>
        </div>

        <div class="preloader-images">
          <div class="image-con con-1">
            <div class="image-1 image" />
          </div>

          <div class="image-con con-2">
            <div class="image-2 image" />
          </div>
        </div>
      </div>
      <h2 class="c-preloader__footer">
        JESS <br />
        CONTE
      </h2>
    </div>
  </div>
</template>

<script>
import gsap from "gsap/all";
import { preloadImage } from "~/utils/index.js";
export default {
  data() {
    return {
      toBePreloaded: [
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718619896/bio_fp0glg.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718618453/header_puxqam.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718558494/hero_nwcawo.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718557539/profile_gz2mqx.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718557920/modelling_aolqc9.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718621582/quote_pi633a.webp",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718642886/further_work_rtk3lp.png",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718643149/work_t7vrck.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718644188/work_new_earth_yk7uop.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718643927/work_conteam_u2z2iu.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718644153/work_new_earth_hvr27g.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718720067/windsor_g5joqy.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718722752/soul_honey_a55uav.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718724655/impress_2_pre4jf.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718804267/harper_willow_dsv40e.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718805060/awards_cid7cm.jpg",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718805059/awards_2_fzdddd.webp",
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718809327/work_quote_cqvz98.jpg",

      ],
      otherstoPreload: [
        "https://res.cloudinary.com/di3otod6k/image/upload/v1718822157/footer_q7wusr.jpg",
      ],
      percentageLoaded: 0,
      isLoaded: false,
      numbersArr: []
    };
  },
  mounted() {
    const preloader = this.$refs.preloader;
    this.preload();
    this.preloadOthers();

    preloader.style.height = `${window.innerHeight}px`;

    window.addEventListener("resize", () => {
      preloader.style.height = `${window.innerHeight}px`;
    });
  },
  methods: {
    async preload() {
      const totalImages = this.toBePreloaded.length;
      let loadedCount = 0;

      const min3Digits = num => {
        if (num < 10) {
          return `00${num}`;
        } else if (num < 99) {
          return `0${num}`;
        }
        return `${num}`;
      };

      this.toBePreloaded.forEach((image, index) => {
        const percentage = Math.floor((100 / totalImages) * (index + 1));
        this.numbersArr = [...this.numbersArr, min3Digits(percentage)];
      });

      await Promise.all(
        this.toBePreloaded.map(async (image, index) => {
          await preloadImage(image);
          loadedCount++;
          const percentage = Math.floor((100 / totalImages) * loadedCount);
          this.percentageLoaded = percentage;

          // Preload first batch of images, and when the preloader percentages are done animating, animate out the preloader
          gsap.to(".p-inner", {
            yPercent: -Math.min(loadedCount * 100, (loadedCount - 2) * 100),
            duration: 4.5,
            ease: "none",
            onComplete: () => {
              if (percentage !== 100) return;
              const tl = gsap.timeline({
                onComplete: () => {
                  this.$store.commit("updateImagesLoaded", true);
                }
              });
              tl.to(".fake-zero", {
                yPercent: -100,
                duration: 1
              })
                .to(
                  ".p-inner",
                  {
                    duration: 1,
                    yPercent: -(loadedCount * 100)
                  },
                  "-=1"
                )
                .set(".preloader-images .con-2", { autoAlpha: 1 });
              tl.from(".preloader-images .con-2", {
                duration: 1.5,
                yPercent: 100,
                ease: "Expo.easeInOut"
              })
                .from(".preloader-images .image-2", {
                  duration: 1.5,
                  yPercent: -100,
                  delay: -1.5,
                  ease: "Expo.easeInOut"
                })
                .set(".preloader-images .con-1", { autoAlpha: 1 })
                .set(".percentages__container", { opacity: 0 })
                .to(".preloader-images .con-2", {
                  duration: 1.5,
                  yPercent: -100,
                  ease: "Expo.easeInOut"
                })
                .to(".preloader-images .image-2", {
                  duration: 1.5,
                  yPercent: 100,
                  delay: -1.5,
                  ease: "Expo.easeInOut"
                })
                .to(".preloader-images .con-1", {
                  duration: 1.5,
                  yPercent: -100,
                  ease: "Expo.easeInOut"
                })
                .to(".preloader-images .image-1", {
                  duration: 1.5,
                  yPercent: 100,
                  delay: -1.5,
                  ease: "Expo.easeInOut"
                })
                .to(".c-preloader__footer", {
                  opacity: 0,
                  delay: -1
                });
            }
          });
        })
      );
    },
    async preloadOthers() {
      this.otherstoPreload.map(async image => {
        await preloadImage(image);
      });
    },
    closeLoader() {
      this.$store.commit("updateImagesLoaded", true);
    }
  }
};
</script>

<style lang="scss" scoped></style>
