<template>
  <div>
    <svg class="cursor" width="32" ref="cursor" height="32" viewBox="0 0 20 20">
      <circle class="cursor__inner" cx="10" cy="10" r="5" />
    </svg>
    <LocomotiveScroll
      ref="scroller"
      :getted-options="{
        direction: 'vertical',
        smooth: true,
        getSpeed: true,
        lerp: 0.1
        // Other options
      }"
    >
      <div class="c-profile">
        <div class="c-profile__header">
          <nuxt-link to="/">
            <AnimatedLink class="c-bezier">
              Close
            </AnimatedLink>
          </nuxt-link>
          <nuxt-link to="/archive">
            <AnimatedLink class="c-bezier">
              Archive
            </AnimatedLink>
          </nuxt-link>
        </div>

        <div class="c-profile__hero">
          <div class="hero__image">
            <img
              src="https://res.cloudinary.com/di3otod6k/image/upload/v1718618453/header_puxqam.jpg"
              alt=""
              data-scroll-speed="1"
            />
          </div>
          <div class="hero-content">
            <h1 class="hero-content__title span-overflow">
              <span class="ov-inner">
                J<span class="fraunces">e</span>ss Cont<span class="fraunces"
                  >e</span
                >
              </span>
            </h1>
            <div class="hero-content__caption">
              <p>Jess Conte</p>
              <p>August 14, 2017</p>
              <p>by @gabrielconte</p>
            </div>
          </div>
        </div>

        <div class="c-profile__headline">
          <h2 class="headline__text">
            <span>Jessica <span class="fraunces">Marie</span> Bauer-Conte</span>
            <span>Jessica <span class="fraunces">Marie</span> Bauer-Conte</span>
            <span>Jessica <span class="fraunces">Marie</span> Bauer-Conte</span>
          </h2>
        </div>
        <div class="c-profile__intro">
          <div class="intro__image">
            <img
              src="https://res.cloudinary.com/di3otod6k/image/upload/v1718619896/bio_fp0glg.jpg"
              alt=""
            />
            <p class="c-caption">
              Jess Conte. &nbsp; <span>January 25, 2021</span>
            </p>
          </div>
          <div class="intro__text">
            <div class="inner">
              <h2>
                is a United States based youtuber & model
              </h2>
              <p class="para-1">
                a dynamic social media influencer and content creator based in the United States,
                captivating millions with her diverse talents. On YouTube, she offers enchanting
                cover songs, beauty tutorials, fashion tips, and home decor inspiration alongside
                her husband, Gabriel Conte. Their daily vlogs, travel adventures, and engaging
                challenges have built a loyal and enthusiastic following.
              </p>
              <p>
                Active on Instagram, Jess's impeccable style and home decor projects consistently
                inspire her audience. Her collaborations with top brands seamlessly blend her
                personal aesthetic with sponsored content. Jess and Gabriel also co-host a popular
                podcast, exploring topics that resonate with their listeners. With her authentic
                charm and creative vision, Jess Conte continues to expand her influence and inspire
                her followers.
              </p>
            </div>
          </div>
        </div>
        <div class="c-profile__editorial">
          <div class="editorial__image">
            <p class="c-caption">
              Jess Conte & Gabriel Conte &nbsp; <span>February 08, 2019</span>
            </p>
          </div>
          <div class="editorial__content first">
            <div class="left">
              <h2>
                “When something doesn't work out, but you still want the best for them."
              </h2>
              <p class="c-caption">
                – Jess Conte. &nbsp; <span>September 21, 2020</span>
              </p>
            </div>
            <div class="right">
              <p>
                Born on July 23, 1996, in Brisbane, Australia, Jess Conte first gained
                recognition through her musical talents and creative videos. She started
                her YouTube journey with cover songs and quickly became known for her design
                skills. After marrying Gabriel in 2016, Jess moved to the United States,
                where they have built a strong online presence together. Their shared and
                individual projects reflect their dedication and creativity, making them
                popular figures in the digital space.
              </p>
            </div>
          </div>
          <div class="editorial__content second">
            <div class="left">
              <p>
                her impact on the online content creation landscape, particularly through her
                innovative approach to combining music, lifestyle, and personal branding.
                Her ability to produce high-quality cover songs while seamlessly integrating
                beauty, fashion, and home decor content has set a new standard for multifaceted
                influencers.
              </p>
            </div>
            <div class="right">
              <div class="image">
                <img
                  src="https://res.cloudinary.com/di3otod6k/image/upload/v1718642886/further_work_rtk3lp.png"
                  alt=""
                />
              </div>
            </div>
          </div>
        </div>

        <div class="c-profile__work">
          <div class="c-profile__work--desktop" ref="works">
            <div class="work__intro">
              <div class="inner">
                <div class="image-con">
                  <div class="intro__image">
                    <img
                      src="https://res.cloudinary.com/di3otod6k/image/upload/v1718643149/work_t7vrck.jpg"
                      alt=""
                    />
                  </div>
                  <p class="c-caption">
                    Jess Conte &nbsp;
                    <span>July 05, 2018</span>
                  </p>
                </div>

                <div class="intro__desc">
                  <h1>W<span class="fraunces">O</span>RK</h1>
                  <p class="first-para">
                    Jess Conte has worked across fashion and
                    media industries as a model, songwriter, vlogger,
                    and content producer.
                  </p>
                  <div class="intro__cta">
                    <button class="cta-button">
                      <animated-arrow />
                    </button>
                    <p>
                      Here are some featured projects, Keep scrolling to see.
                    </p>
                  </div>
                </div>
              </div>
            </div>
            <div class="work__companies">
              <div class="conteam-newearth">
                <div class="conteam">
                  <div class="conteam__left">
                    <h2>CONTEAM</h2>
                    <div class="conteam__image1">
                      <img
                        src="https://res.cloudinary.com/di3otod6k/image/upload/v1718644188/work_new_earth_yk7uop.jpg"
                        alt="Conteam clothing"
                        class="skew-image"
                      />
                    </div>
                    <animated-arrow
                      href="https://www.instagram.com/newearth/?hl=en"
                    />
                  </div>
                  <div class="conteam__right">
                    <div class="conteam__image2">
                      <img
                        src="https://res.cloudinary.com/di3otod6k/image/upload/v1718643927/work_conteam_u2z2iu.jpg"
                        alt="Conteam clothing"
                        class="skew-image"
                      />
                    </div>
                    <p>
                      Collaboration with Gabriel Conte on the creation of
                      Conteam premium, faith-based clothing brand.
                    </p>
                  </div>
                </div>
                <div class="newearth">
                  <div>
                    <div class="newearth__image">
                      <img
                        src="https://res.cloudinary.com/di3otod6k/image/upload/v1718644153/work_new_earth_hvr27g.jpg"
                        alt="New Earth logo"
                      />
                    </div>
                    <div class="newearth__desc">
                      <h3>NEW EARTH</h3>
                      <p>Rebranded Conteam to New Earth.</p>
                    </div>
                  </div>
                </div>
              </div>

              <div class="windsor">
                <div class="windsor__image">
                  <img
                    src="https://res.cloudinary.com/di3otod6k/image/upload/v1718720067/windsor_g5joqy.jpg"
                    alt="Oxlade at windsor"
                    class="skew-image"
                  />
                </div>
                <div class="windsor__desc">
                  <p>
                    collaborated with Windsor to bring the spring 2020 fashion collection.
                  </p>
                  <animated-arrow href="https://www.windsorstore.com/blogs/lifestyle/2020-spring-collection-by-influencer-jess-conte" />
                </div>
                <h1>WINDSOR</h1>
              </div>

              <div class="music-instruments-singing-ga">
                <div class="music-instruments-singing">
                  <h3>MUSIC INSTRUMENTS <br />& SINGING</h3>
                  <p>
                    Released her own covers on some songs, as early as 2014 on her
                    youtube channel.
                  </p>
                </div>
                <div class="soul_honey">
                  <div class="soul_honey__image">
                    <img
                      src="https://res.cloudinary.com/di3otod6k/image/upload/v1718722752/soul_honey_a55uav.jpg"
                      alt=""
                      class="skew-image"
                    />
                  </div>
                  <div class="soul_honey__desc">
                    <animated-arrow href="https://www.soulhoneyclothing.com/" />
                    <div>
                      <h1>
                        SOUL <br /> HONEY
                      </h1>
                      <p>
                        Collaborated with Soul Honey clothing company in 2017.
                      </p>
                    </div>
                  </div>
                </div>

                <div class="under_the_covers">
                  <div class="under_the_covers__label">
                    <div class="under_the_covers__disclaimer">
                      <span>*</span>
                      <p>
                        Extended Plays
                      </p>
                    </div>
                    <h3>2017</h3>
                  </div>
                  <h2 class="under_the_covers__title">
                    UNDER THE COVERS
                  </h2>
                  <div class="under_the_covers__story">
                    <div class="under_the_covers__desc">
                      <p>
                        recorded an EP titled Under the Covers, with Gabriel Conte, consisting of five acoustic covers of popular love songs.
                      </p>
                    </div>
                    <animated-arrow
                      href="https://www.amazon.com/Under-Covers-Vol-Jess-Gabriel/dp/B074CH6VLY"
                    />
                  </div>
                </div>
              </div>

              <div class="impress">
                <div class="impress__top">
                  <div class="image-1">
                    <img
                      src="https://res.cloudinary.com/di3otod6k/image/upload/v1718724464/imPRESS_atzifp.png"
                      alt=""
                    />
                  </div>
                  <div class="image-2">
                    <img
                      src="https://res.cloudinary.com/dmwfd0zhh/image/upload/q_auto,f_auto/v1621524466/Korty/kortybbn2_dixrhc.jpg"
                      alt=""
                    />
                    <p>
                      collaborated with imPRESS manicure in 2021.
                    </p>
                  </div>
                </div>
                <h2>IMPRESS</h2>
              </div>
              <div class="harper_willow">
                <img
                  src="https://res.cloudinary.com/di3otod6k/image/upload/v1718804267/harper_willow_dsv40e.jpg"
                  alt=""
                  class="harper_willow__image skew-image"
                />
                <div class="harper_willow__panel">
                  <h2>
                    HARPER & <br /> WILLOW
                  </h2>
                  <p>
                    Started a lifestyle-based stationary brand in 2018.
                  </p>
                  <animated-arrow href="https://x.com/harpernwillow?lang=en" />
                </div>
              </div>
              <div class="awards">
                <div class="awards__left">
                  <img
                    src="https://res.cloudinary.com/di3otod6k/image/upload/v1718805060/awards_cid7cm.jpg"
                    alt=""
                    class="skew-image"
                  />
                </div>
                <div class="awards__right">
                  <div class="awards__top">
                    <div class="awards__image">
                      <img
                        src="https://res.cloudinary.com/di3otod6k/image/upload/v1718805059/awards_2_fzdddd.webp"
                        alt=""
                      />
                    </div>
                    <div class="awards__desc">
                      <animated-arrow href="https://www.instagram.com/jess/p/BGoI-FTyIHR/" />
                      <p>
                        Attended multiple award shows with Gabriel Conte.
                      </p>
                    </div>
                  </div>
                  <h1>
                    AWARDS
                  </h1>
                </div>
              </div>
            </div>
            <div class="work__quote">
              <div>
                <div class="desc">
                  <animated-arrow
                    href="https://www.youtube.com/@JessConte"
                  />
                  <p>
                    Now, Jess is passionately involved with her YouTube channel, Instagram,
                    and fashion collaboration with her husband Gabriel.
                  </p>
                </div>
                <h1>THE CHOICES THAT</h1>
                <div class="row-2">
                  <h1><span class="fraunces">Lead</span> &nbsp;TO THE <span class="fraunces">Life</span></h1>
                  <div class="row-image">
                    <img
                      src="https://res.cloudinary.com/di3otod6k/image/upload/v1718809327/work_quote_cqvz98.jpg"
                      alt=""
                    />
                  </div>
                </div>
                <h1>YOU REALLY WANT.</h1>
              </div>
            </div>
          </div>

          <div class="c-profile__work--mobile show-tablet">
            <h1 class="first-heading">W<span class="fraunces">O</span>RK</h1>
            <p class="first-para">
              Jess Conte has worked across fashion and
              media industries as a model, songwriter, vlogger,
              and content producer.
            </p>
            <div class="intro__image">
              <div />
            </div>

            <div class="work__places">
              <a href="/" target="__blank" class="right">CONTEAM</a>
              <a href="/" target="__blank" class="right">NEW EARTH</a>
              <a href="/" target="__blank" class="right">WINDSOR</a>
              <a href="/" target="__blank" class="center music-instruments-singing">
                <span>MUSIC INSTRUMENTS & SINGING</span>
              </a>
              <a href="/" target="__blank" class="center">
                <span>SOUL HONEY</span>
              </a>
              <a href="/" target="__blank" class="center"
                >UND<span class="fraunces">E</span
                >R TH<span class="fraunces">E</span
                > COV<span class="fraunces">E</span>R</a
              >
              <a href="/" target="__blank">IMPRESS</a>
              <a href="/" target="__blank">HARPER & WILLOW</a>
              <a href="/" target="__blank">AWARDS</a>
            </div>

            <div class="work__quote">
              <img
                src="https://res.cloudinary.com/di3otod6k/image/upload/v1718809327/work_quote_cqvz98.jpg"
                alt=""
              />

              <h1>
                THE CHOICES THAT
                <span class="fraunces">Lead</span> &nbsp;TO THE <span class="fraunces"
                  >LIFE</span> THAT YOU REALLY WANT.
              </h1>
              <p>
                Now, Jess is passionately involved with her YouTube channel, Instagram,
                and fashion collaboration with her husband Gabriel.
              </p>
            </div>
          </div>
        </div>

        <div class="c-profile__footer">
          <div class="inner-con">
            <div class="footer__left show-desktop">
              <button class="credits-link" @click="openModal">
                <div class="c-inner">
                  <animated-link class="c-bezier">
                    credits
                  </animated-link>
                </div>
              </button>
              <p>
                Jess Conte <br />
                <a
                  href="https://josephchay@netlify.app/"
                  target="__blank"
                  style="text-decoration: underline;"
                  >Made by Joseph</a
                >
              </p>
              <div class="footer__image">
                <img
                  src="https://res.cloudinary.com/di3otod6k/image/upload/v1718822157/footer_q7wusr.jpg"
                  alt=""
                />
              </div>
            </div>
            <div class="footer__center">
              <h1>Thank <span class="fraunces">you!</span></h1>
              <div class="c-bottom">
                <div class="bottom__left">
                  <p class="c-desc">
                    If you enjoyed going through this web experience, consider
                    sharing it on social media so other people get to see it.
                  </p>
                  <div class="socials">
                    <a href="/" target="_blank" class="social">
                      <animated-link class="c-bezier">
                        Tweet
                      </animated-link>
                    </a>
                    <a href="/" target="_blank" class="social">
                      <animated-link class="c-bezier">
                        Post on Instagram
                      </animated-link>
                    </a>
                  </div>
                  <p class="c-facebook show-desktop">
                    If you still use Facebook, we want better for you.
                  </p>
                </div>
                <div class="bottom__right">
                  <p>
                    Have a look at the Credits and support all the awesome
                    creators whose works were featured, If you still want to
                    continue the experience, head over to the archive page.
                  </p>

                  <button class="credits-link" @click="openModal">
                    <div class="c-inner">
                      <animated-link class="c-bezier">
                        credits
                      </animated-link>
                    </div>
                  </button>
                </div>
              </div>
            </div>
            <div class="footer__right">
              <nuxt-link class="c-circular-link" to="/archive">
                <circular-link>
                  View Jess's Archive
                </circular-link>
              </nuxt-link>
              <p class="show-mobile">
                Jess Conte by her own
              </p>
            </div>
          </div>
        </div>
      </div>
    </LocomotiveScroll>
  </div>
</template>

<script>

import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import AnimatedLink from "../components/AnimatedLink/AnimatedLink.vue";
import Arrow from "../components/Arrow.vue";
import CircularLink from "../components/CircularLink/CircularLink.vue";
import AnimatedArrow from "../components/AnimatedArrow.vue";
import { ScrollToPlugin } from "gsap/all";
import { Cursor } from "~/animations/cursor";

gsap.registerPlugin(ScrollTrigger, ScrollToPlugin);

export default {
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
        duration: 2
      })
        .from(
          ".hero__image img",
          {
            duration: 1,
            scale: 1.2,
            ease: "power2.out"
          },
          "-=2"
        )
        .from(
          ".span-overflow .ov-inner",
          {
            yPercent: 100,
            duration: 1,
            ease: "power2.out"
          },
          "-=2"
        );
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
  components: { AnimatedLink, Arrow, CircularLink, AnimatedArrow },
  mounted() {
    const worksRef = this.$refs.works;
    this.beginCursor();

    this.initScrolltrigger();
    this.marqueeAnimation();
    this.heroImageAnimation();
    this.worksAnimation(worksRef);
    this.musicInstrumentsSingingAnimation();

    this.$nuxt.$emit("update-locomotive");
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
    },
    initScrolltrigger() {
      const locomotive = this.$refs.scroller.locomotive;
      locomotive.on("scroll", ScrollTrigger.update);

      ScrollTrigger.scrollerProxy(locomotive.el, {
        scrollTop(value) {
          return arguments.length
            ? locomotive.scrollTo(value, 0, 0)
            : locomotive.scroll.instance.scroll.y;
        },
        scrollLeft(value) {
          return arguments.length
            ? locomotive.scrollTo(value, 0, 0)
            : locomotive.scroll.instance.scroll.x;
        },

        getBoundingClientRect() {
          return {
            top: 0,
            left: 0,
            width: window.innerWidth,
            height: window.innerHeight
          };
        }
      });
    },
    marqueeAnimation() {
      gsap.to(".headline__text", {
        scrollTrigger: {
          trigger: ".c-profile__headline",
          scroller: this.$refs.scroller.locomotive.el,
          scrub: true,
          start: "top 90%",
          end: "bottom 10%"
          // markers: true
        },
        xPercent: -50
      });
    },
    musicInstrumentsSingingAnimation() {
      gsap.to(".music-instruments-singing span", {
        scrollTrigger: {
          trigger: ".music-instruments-singing",
          scroller: this.$refs.scroller.locomotive.el,
          scrub: true,
          start: "top 40%",
          end: "bottom top"
          // markers: true
        },
        xPercent: -50
      });
    },
    heroImageAnimation() {
      gsap.to(".hero__image img", {
        scrollTrigger: {
          trigger: ".c-profile__headline",
          scroller: this.$refs.scroller.locomotive.el,
          scrub: 1,
          start: "top bottom",
          end: "bottom center"
        },
        scale: 1.17
        // ease: "none"
      });
      gsap.to(".hero__image", {
        scrollTrigger: {
          trigger: ".c-profile__headline",
          scroller: this.$refs.scroller.locomotive.el,
          scrub: true,
          start: "top bottom",
          end: "bottom center"
        },
        y: 20
        // ease: "none"
      });
    },
    worksAnimation(container) {
      let isScrollForward = true;
      const proxy = { skew: 0, bounce: 1 },
        skewSetter = gsap.quickSetter(".skew-image", "skewX", "deg"),
        // scaleSetter = gsap.quickSetter(".scaleEl", "scaleY"),
        clamp = gsap.utils.clamp(-30, 30);
      // scaleClamp = gsap.utils.clamp(0.95, 1.1);
      const timeline = gsap.timeline();
      const under_the_coversDesc = document.querySelector(".under_the_covers__desc");
      const ctaButton = document.querySelector(".cta-button");
      const workSection = document.querySelector(".work__companies");

      const anim = gsap.to(container, {
        x: () => {
          return -(container.scrollWidth - innerWidth);
        },
        ease: "none",
        overwrite: "auto",
        scrollTrigger: {
          trigger: container,
          invalidateOnRefresh: true,
          scroller: this.$refs.scroller.locomotive.el,
          pin: true,
          scrub: 1,

          end: () => "+=" + (container.offsetWidth + innerWidth),

          onUpdate(self) {
            let skew = clamp(self.getVelocity() / -230);

            const direction = self.direction;
            const snapDifference =
              self.progress * self.end - (self.end - window.innerWidth);

            if (isScrollForward) {
              if (snapDifference > window.innerWidth * 0.5) {
                window.innerWidth > 768 && self.scroll(self.end);
                isScrollForward = false;
              }
            }

            if (
              direction === -1 &&
              snapDifference > window.innerWidth * 0.6 &&
              snapDifference < window.innerWidth * 0.9
            ) {
              const snapProgress =
                window.innerWidth / (container.scrollWidth - window.innerWidth);
              const differenceEndStart = self.end - self.start;
              const snapDeduction = snapProgress * differenceEndStart;

              window.innerWidth > 768 &&
                self.scroll(self.end - (snapDeduction + 2));

              setTimeout(() => {
                isScrollForward = true;
              }, 1000);
            }

            if (Math.abs(skew) > Math.abs(proxy.skew)) {
              proxy.skew = skew;
              // proxy.bounce = bounce;
              gsap.to(proxy, {
                skew: 0,
                duration: 0.7,
                ease: "power3",
                overwrite: true,
                onUpdate: () => {
                  skewSetter(proxy.skew);
                  // scaleSetter(proxy.bounce);
                }
              });
            }
          }
          // markers: true
        }
      });

      // Get the scrolltrigger instance on the scroll animation
      const self = anim.scrollTrigger;
      ctaButton.addEventListener("click", () => {
        const snapProgress =
          window.innerWidth / (container.scrollWidth - window.innerWidth);
        const differenceEndStart = self.end - self.start;
        const snapDeduction = snapProgress * differenceEndStart;

        self.scroll(self.start + snapDeduction + 50);
      });

      // Rotate the under_the_covers circle as it enters/exits the viewport
      timeline.to(under_the_coversDesc, {
        rotate: "2deg",
        overwrite: "auto",
        scrollTrigger: {
          scrub: 1,
          // markers: true,
          invalidateOnRefresh: true,
          scroller: this.$refs.scroller.locomotive.el,
          start: () =>
            container.scrollWidth -
            under_the_coversDesc.parentNode.offsetLeft -
            under_the_coversDesc.parentNode.getBoundingClientRect().width -
            under_the_coversDesc.getBoundingClientRect().width +
            20,
          end: () =>
            under_the_coversDesc.parentNode.offsetLeft -
            under_the_coversDesc.parentNode.getBoundingClientRect().width
        }
      });

      // force 3D for performance
      gsap.set(".skew-image", {
        transformOrigin: "right center",
        force3D: true
      });

      // Update locomotive on resize
      ScrollTrigger.addEventListener("refresh", () => {
        this.$nuxt.$emit("update-locomotive");
      });

      ScrollTrigger.refresh();
    }
  }
};
</script>

<style lang="scss" scoped></style>
