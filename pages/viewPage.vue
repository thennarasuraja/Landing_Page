<template>
  <div class="font-plusJakartaSans">
    <div class="confetti" v-if="showConfetti" ref="confettiContainer">
      <div
        v-for="n in 60"
        :key="n"
        class="confetti-piece"
        :style="getConfettiStyle(n)"
      ></div>
    </div>
    <div class="popper" v-if="showPopper" ref="popper"></div>
    <div
      class="flex justify-center bg-gradient-to-t to-[#F2F2F2] h-[286px] md:h-[306px] lg:h-[238px] xl:h-[280px] mt-[6px] mx-[6px] from-[#FFF] rounded-[24px] rounded-b-none"
    >
      <div class="max-w-[1180px] w-full">
        <div class="max-w-[1180px] w-full">
          <div
            class="flex flex-col xl:gap-[48px] lg:gap-[38px] md:gap-[28px] lg:px-0 md:px-[34px] gap-[20px]"
          >
            <div class="flex justify-center">
              <div
                class="md:px-[20px] px-[16px] bg-white shadow-sm rounded-[12px] py-[8px] rounded-t-none"
              >
                <img
                  class="w-[68px] h-[24px] md:w-[68px] md:h-[24px] lg:w-[68px] lg:h-[24px] xl:w-[72px] xl:h-[26px] object-fill"
                  src="https://gardeniaschools.com/images/logo.png"
                  alt="logo"
                />
              </div>
            </div>
          </div>
          <div class="flex justify-center">
            <div
              class="flex justify-center lg:px-[34px] pb-[60px] px-[14px] md:px-[34px] flex-col lg:pt-[36px] md:pt-[28px] pt-[20px] xl:pt-[48px]"
            >
              <div
                class="flex flex-col xl:gap-[40px] lg:gap-[20px] md:gap-[20px] gap-[20px]"
              >
                <div
                  class="flex xl:gap-[12px] justify-center lg:gap-[12px] md:gap-[4px] gap-[4px]"
                >
                  <div class="flex items-center">
                    <img
                      class="lg:w-[48px] lg:h-[48px] h-[28px] w-[28px] md:w-[32px] md:h-[32px]"
                      :src="gif"
                    />
                  </div>
                  <div class="flex items-center">
                    <div
                      class="text-center font-plusJakartaSans md:text-[36px] md:leading-[40px] text-[26px] leading-[32px] lg:text-[36px] lg:leading-[40px] xl:text-[40px] xl:leading-[48px] not-italic font-bold"
                    >
                      <div class="">
                        <span
                          class="flex text gradient-text"
                          :style="getStyle(index)"
                          @animationend="handleAnimationEnd(index)"
                        >
                          <transition>
                            <p class="zoom-text gradient-text">
                              Congratulations!
                            </p>
                          </transition>
                        </span>
                      </div>
                    </div>
                  </div>
                  <div class="flex items-center">
                    <img
                      class="lg:w-[48px] -rotate-90 lg:h-[48px] h-[28px] w-[28px] md:w-[32px] md:h-[32px]"
                      :src="gif"
                    />
                  </div>
                </div>
                <div
                  class="text-center fadeInUp font-plusJakartaSans text-[16px] leading-[24px] lg:text-[18px] lg:leading-[28px] xl:text-[20px] xl:leading-[28px] md:text-[18px] md:leading-[28px] font-medium not-italic text-neutral-500"
                >
                  {{ user.childName }} have successfully registered for the
                </div>
              </div>
              <div class="fadeInUp">
                <div
                  class="xl:pt-[8px] lg:pt-[8px] md:pt-[6px] pt-[6px] fadeInUp"
                >
                  <div class="flex justify-center">
                    <div class="text-center md:text-center lg:text-center">
                      <span
                        class="font-plusJakartaSans xl:text-[40px] md:pl-[8px] lg:pl-0 text-[26px] md:text-[36px] lg:text-[36px] not-italic linear-text font-bold lg:leading-[40px] md:leading-[40px] leading-[32px] xl:leading-[48px]"
                      >
                        Our Team
                      </span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      user: JSON.parse(this.$route.query.data),
      showText: false,
      showConfetti: false,
      characters: "Congratulations!".split(""),
      showPopper: false,

      gif: "https://hubble.cdn.chittiapp.com/cdn_uploads/2b341ad0-3832-11ef-9502-6d1b78ea5228_Party-Popper.gif",
    };
  },
  mounted() {
    const fadeInElements = this.$el.querySelectorAll(".fadeInUp");
    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          if (entry.isIntersecting) {
            entry.target.classList.add("active");
            observer.unobserve(entry.target);
          }
        });
      },
      {
        threshold: 0.1,
      }
    );

    fadeInElements.forEach((el) => {
      observer.observe(el);
    });
    this.handleAnimationEnd();
  },
  methods: {
    getStyle(index) {
      return {
        animationDelay: `${index * 0.2}s`,
      };
    },
    handleAnimationEnd() {
      this.show = true;
      this.showPopper = true;
      setTimeout(() => {
        this.triggerPartyPopper();
      }, 50);
    },
    triggerPartyPopper() {
      this.showConfetti = true;
      const popper = this.$refs.popper;
      setTimeout(() => {
        popper.style.animation = "none";
      }, 50);
      const confettiContainer = this.$refs.confettiContainer;
      confettiContainer.style.animation = "none";
      void confettiContainer.offsetWidth;
    },
    getConfettiStyle(index) {
      const colors = [
        "#00D3F0",
        "#19C261",
        "#0A1FD1",
        "#E92AF2",
        "#0f0",
        "#F22A54",
        "#ff0",
        "#f0f",
        "#0ff",
        "#f00",
        "#0f0",
        "#00f",
      ];
      const size = Math.random() * 10 + 5;
      const left = Math.random() * 100;
      const delay = Math.random() * 2;
      return {
        backgroundColor: colors[index % colors.length],
        width: `${size}px`,
        height: `${size}px`,
        left: `${left}%`,
        animationDelay: `${delay}s`,
      };
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Averia+Libre:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Averia+Sans+Libre:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Averia+Serif+Libre:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Dancing+Script:wght@400..700&family=Elsie:wght@400;900&family=Mulish:ital,wght@0,200..1000;1,200..1000&family=Plus+Jakarta+Sans:ital,wght@0,200..800;1,200..800&family=Protest+Revolution&family=Protest+Riot&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&family=Sixtyfour:BLED@0..100&family=UnifrakturMaguntia&display=swap");
.letter-spacing {
  letter-spacing: 0.4px;
}
.fadeInUp {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.3s ease-out, transform 0.4s ease-out;
}

.fadeInUp.active {
  opacity: 2;
  transform: translateY(0);
}
.gradient-text {
  background: linear-gradient(
    90deg,
    #3b82f6 0%,
    #06b6d4 32.9%,
    #ffc107 65.4%,
    #e64f44 100%
  );
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.background-color {
  background: linear-gradient(
    90deg,
    rgba(59, 130, 246, 0.06) 0%,
    rgba(6, 182, 212, 0.06) 100%
  );
}
.linear-text {
  background: linear-gradient(90deg, #3b82f6, #06b6d4);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.text {
  display: inline-block;
  animation: bounce 2s ease-in-out forwards;
}

@keyframes bounce {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateY(0);
  }
  40% {
    transform: translateY(0);
  }
  60% {
    transform: translateY(-1px);
  }
}
.popper {
  position: absolute;
  top: 20%;
  left: 50%;
  transform: translateX(-50%);
  width: 30px;
  height: 70px;
  background-color: gold;
  opacity: 0;
  z-index: 10;
}

.confetti {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  pointer-events: none;
  z-index: 10;
}

.confetti-piece {
  position: absolute;
  top: -30px;
  width: 30px;
  height: 70px;
  opacity: 1;
  animation: fall 3s ease-out forwards;
  animation-fill-mode: forwards;
  z-index: 10;
}

@keyframes fall {
  to {
    transform: translateY(100vh);
    opacity: 0;
  }
}

@keyframes fade-in-out {
  0%,
  100% {
    opacity: 0;
  }
  50% {
    opacity: 1;
  }
}
@keyframes zoomInFromSmall {
  0% {
    transform: scale(0.5);
    opacity: 0;
  }
  100% {
    transform: scale(1);
    opacity: 1;
  }
}

.zoom-text {
  display: inline-block;
  animation: zoomInFromSmall 0.5s ease-out forwards;
}
</style>
