<template>
  <div class="w-full h-full">
    <div class="bg-white font-PlusJakartaSans min-h-screen overflow-auto">
      <div
        class="flex justify-center bg-gradient-to-t to-[#F2F2F2] h-[300px] my-[6px] mx-[6px] from-[#FFF] rounded-[24px] rounded-b-none"
      >
        <div class="max-w-[1180px] w-full">
          <div class="flex flex-col">
            <div class="flex justify-center">
              <div
                class="md:px-[20px] px-[16px] bg-white shadow-sm rounded-[12px] py-[8px] rounded-t-none"
              >
                <img
                  class="w-[68px] h-[24px] md:w-[68px] md:h-[24px] lg:w-[68px] lg:h-[24px] xl:w-[92px] xl:h-[36px] object-fill"
                  src="https://gardeniaschools.com/images/logo.png"
                  alt="logo"
                />
              </div>
            </div>
          </div>

          <div class="flex lg:gap-[32px] xl:gap-[40px] w-full max-w-[1180px]">
            <div
              class="flex w-full lg:w-[608px] xl:w-[780px] pt-[20px] md:pt-[28px] xl:pt-[36px] flex-col"
            >
              <div class="xl:px-0 lg:px-[32px] md:px-[40px] px-[14px]">
                <div
                  class="xl:pt-[8px] pt-[6px] xl:w-[650px] lg:pt-[6px] md:pt-[6px] fadeInUp"
                >
                  <div class="">
                    <span
                      class="font-plusJakartaSans xl:text-[40px] text-[32px] md:text-[36px] lg:text-[36px] not-italic text-black font-bold lg:leading-[40px] md:leading-[40px] leading-[38px] xl:leading-[48px]"
                    >
                      Gardenia
                    </span>

                    <span
                      class="font-plusJakartaSans text-[32px] leading-[38px] xl:text-[40px] lg:text-[40px] md:text-[40px] not-italic gradient-text font-bold md:leading-[48px] lg:leading-[48px] xl:leading-[48px]"
                    >
                      {{ displayText1 }}
                    </span>
                  </div>
                </div>
                <div
                  class="pt-[12px] lg:hidden xl:hidden md:block block fadeInUp"
                >
                  <div
                    class="text-neutral-500 font-plusJakartaSans leading-[24px] md:text-[18px] md:leading-[28px] text-[16px] lg:text-[18px] lg:leading-[28px] xl:text-[20px] not-italic xl:leading-[28px] font-medium"
                  >
                    Cultivating a Love for Learning
                  </div>
                </div>
                <div class="pt-[12px] lg:block hidden md:hidden fadeInUp">
                  <div
                    class="text-neutral-500 font-plusJakartaSans leading-[24px] md:text-[18px] md:leading-[28px] text-[16px] lg:text-[18px] lg:leading-[28px] xl:text-[20px] not-italic xl:leading-[28px] font-medium"
                  >
                    Cultivating a Love for Learning
                  </div>
                </div>

                <div
                  class="pt-[16px] lg:pt-[16px] md:pt-[16px] xl:pt-[20px] flex flex-col gap-[4px] fadeInUp"
                >
                  <div class="flex gap-[5px]">
                    <div class="flex gap-[2px]">⭐⭐⭐⭐⭐</div>
                  </div>
                  <div class="flex gap-[4px] items-center">
                    <div
                      class="text-neutral-800 text-[14px] leading-[20px] font-plusJakartaSans not-italic font-bold"
                    >
                      500+
                    </div>
                    <div
                      class="text-neutral-500 font-plusJakartaSans text-[14px] not-italic font-medium leading-[20px]"
                    >
                      Happy Students
                    </div>
                    <div class="flex items-center">😄</div>
                  </div>
                </div>
                <div
                  class="fadeInUp py-[20px] lg:py-[20px] md:py-[20px] xl:py-[28px] overflow-hidden rounded-[18px] xl:rounded-[26px]"
                >
                  <div
                    class="flex flex-col items-center gap-6 md:gap-[34px] lg:gap-10 m lg:flex-row"
                  >
                    <div
                      class="flex items-center justify-center mt-10 space-x-2"
                    >
                      <div
                        v-for="(image, index) in images"
                        :key="index"
                        :class="[
                          'relative overflow-hidden rounded-lg shadow-lg lg:w-full md:w-[230px] w-[140px]',
                          imageClass(index),
                        ]"
                      >
                        <img :src="image.src" class="object-cover h-full" />
                      </div>
                    </div>
                  </div>
                </div>

                <!-- for mobile -->
                <div class="block md:hidden lg:hidden xl:hidden">
                  <div class="pt-[20px] fadeInUp">
                    <div>
                      <div class="flex flex-col gap-[12px]">
                        <div
                          @click="createAdmission()"
                          class="bg-gradient-to-l w-full xl:h-[48px] animation md:h-[44px] h-[44px] from-[#06B6D4] to-[#22B2AA] relative cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                        >
                          <div class="absolute top-[6px] left-[6px]">
                            <div
                              class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div class="absolute top-[6px] right-[6px]">
                            <div
                              class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div
                            class="absolute top-[10px] w-full flex justify-center"
                          >
                            <div class="flex items-center px-[24px] gap-[4px]">
                              <div
                                class="text-white text-center font-plusJakartaSans text-[14px] leading-[20px] xl:text-[16px] not-italic font-bold xl:leading-[24px]"
                              >
                                Admission
                              </div>
                            </div>
                          </div>

                          <div class="pt-[46px]">
                            <div
                              class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute"
                            >
                              <div class="absolute bottom-[6px] left-[4px]">
                                <div
                                  class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                              <div class="absolute bottom-[6px] right-[4px]">
                                <div
                                  class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                            </div>
                          </div>
                        </div>

                        <div
                          @click="makeCall()"
                          class="bg-color w-full xl:h-[48px] md:h-[44px] h-[44px] animation relative cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                        >
                          <div class="absolute top-[6px] left-[6px]">
                            <div
                              class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div class="absolute top-[6px] right-[6px]">
                            <div
                              class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div
                            class="absolute top-[10px] w-full flex justify-center"
                          >
                            <div class="flex items-center px-[24px] gap-[4px]">
                              <div
                                class="gradient-text text-center font-plusJakartaSans text-[14px] xl:text-[16px] not-italic font-bold leading-[20px] xl:leading-[24px]"
                              >
                                Contact Us
                              </div>
                            </div>
                          </div>

                          <div class="pt-[46px]">
                            <div
                              class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute rg-color"
                            >
                              <div class="absolute bottom-[6px] left-[4px]">
                                <div
                                  class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                              <div class="absolute bottom-[6px] right-[4px]">
                                <div
                                  class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>

                    <div class="hidden md:block lg:hidden xl:hidden">
                      <div class="flex gap-[12px]">
                        <div
                          @click="createAdmission()"
                          class="bg-gradient-to-l xl:h-[48px] w-full animation md:h-[44px] h-[44px] from-[#06B6D4] to-[#22B2AA] relative cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                        >
                          <div class="absolute top-[6px] left-[6px]">
                            <div
                              class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div class="absolute top-[6px] right-[6px]">
                            <div
                              class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div
                            class="absolute top-[10px] w-full flex justify-center"
                          >
                            <div class="flex items-center px-[24px] gap-[4px]">
                              <div
                                class="text-white text-center font-plusJakartaSans text-[16px] not-italic font-bold leading-[24px]"
                              >
                                Admission
                              </div>
                            </div>
                          </div>

                          <div class="pt-[46px]">
                            <div
                              class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute"
                            >
                              <div class="absolute bottom-[6px] left-[4px]">
                                <div
                                  class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                              <div class="absolute bottom-[6px] right-[4px]">
                                <div
                                  class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                            </div>
                          </div>
                        </div>

                        <div
                          @click="makeCall()"
                          class="bg-color w-full xl:h-[48px] md:h-[44px] h-[44px] relative animation cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                        >
                          <div class="absolute top-[6px] left-[6px]">
                            <div
                              class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div class="absolute top-[6px] right-[6px]">
                            <div
                              class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                            ></div>
                          </div>
                          <div
                            class="absolute top-[10px] w-full flex justify-center"
                          >
                            <div class="flex items-center px-[24px] gap-[4px]">
                              <div
                                class="gradient-text text-center font-plusJakartaSans text-[16px] not-italic font-bold leading-[24px]"
                              >
                                Contact Us
                              </div>
                            </div>
                          </div>

                          <div class="pt-[46px]">
                            <div
                              class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute rg-color"
                            >
                              <div class="absolute bottom-[6px] left-[4px]">
                                <div
                                  class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                              <div class="absolute bottom-[6px] right-[4px]">
                                <div
                                  class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                                ></div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

                <!-- for md screen -->
                <div class="">
                  <div class="hidden md:block lg:hidden xl:hidden">
                    <div class="flex gap-[12px] fadeInUp">
                      <div
                        @click="createAdmission()"
                        class="bg-gradient-to-l xl:h-[48px] w-full animation md:h-[44px] h-[44px] from-[#06B6D4] to-[#22B2AA] relative cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                      >
                        <div class="absolute top-[6px] left-[6px]">
                          <div
                            class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                          ></div>
                        </div>
                        <div class="absolute top-[6px] right-[6px]">
                          <div
                            class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                          ></div>
                        </div>
                        <div
                          class="absolute top-[10px] w-full flex justify-center"
                        >
                          <div class="flex items-center px-[24px] gap-[4px]">
                            <div
                              class="text-white text-center font-plusJakartaSans text-[14px] not-italic font-bold leading-[20px]"
                            >
                              Admission
                            </div>
                          </div>
                        </div>

                        <div class="pt-[46px]">
                          <div
                            class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute"
                          >
                            <div class="absolute bottom-[6px] left-[4px]">
                              <div
                                class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                            <div class="absolute bottom-[6px] right-[4px]">
                              <div
                                class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                          </div>
                        </div>
                      </div>

                      <div
                        @click="makeCall()"
                        class="bg-color w-full xl:h-[48px] md:h-[44px] h-[44px] animation relative cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                      >
                        <div class="absolute top-[6px] left-[6px]">
                          <div
                            class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                          ></div>
                        </div>
                        <div class="absolute top-[6px] right-[6px]">
                          <div
                            class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                          ></div>
                        </div>
                        <div
                          class="absolute top-[12px] w-full flex justify-center"
                        >
                          <div class="flex items-center gap-[4px]">
                            <div
                              class="gradient-text text-center font-plusJakartaSans text-[14px] not-italic font-bold leading-[20px]"
                            >
                              Contact Us
                            </div>
                          </div>
                        </div>

                        <div class="pt-[46px]">
                          <div
                            class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute rg-color"
                          >
                            <div class="absolute bottom-[6px] left-[4px]">
                              <div
                                class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                            <div class="absolute bottom-[6px] right-[4px]">
                              <div
                                class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div class="hidden lg:block">
              <div class="lg:pt-[48px] xl:pt-[48px] fadeInUp">
                <div
                  class="h-[260px] border-neutral-100 lg:px-[24px] bg-white border rounded-[16px] xl:px-[28px] py-[28px] shadow border-neutral-100' xl:w-[360px] lg:w-[304px]"
                >
                  <div>
                    <div class="xl:w-[304px] lg:w-[256px]">
                      <div class="flex flex-col w-full gap-[16px]">
                        <div
                          class="text-black font-plusJakartaSans text-[20px] not-italic font-semibold leading-[28px]"
                        >
                          Start Admission Today!
                        </div>
                      </div>
                      <div class="xl:pt-[24px] lg:pt-[20px]">
                        <div class="flex gap-[4px] items-center">
                          <div
                            class="text-neutral-800 text-[14px] leading-[20px] font-plusJakartaSans not-italic font-bold"
                          >
                            500+
                          </div>
                          <div
                            class="text-neutral-500 font-plusJakartaSans text-[14px] not-italic font-medium leading-[20px]"
                          >
                            Happy Students
                          </div>
                          <div class="flex items-center">😄</div>
                        </div>
                      </div>
                      <div class="pt-[12px] lg:pb-[22px] xl:pb-[26px]">
                        <div
                          class="flex flex-col gap-[16px] xl:w-[304px] lg:w-[256px]"
                        >
                          <div
                            @click="createAdmission()"
                            class="bg-gradient-to-l xl:h-[48px] md:h-[44px] animation h-[44px] from-[#06B6D4] to-[#22B2AA] relative cursor-pointer pt-[2px] rounded-[8px]"
                          >
                            <div class="absolute top-[6px] left-[6px]">
                              <div
                                class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                            <div class="absolute top-[6px] right-[6px]">
                              <div
                                class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                            <div
                              class="absolute top-[10px] w-full flex justify-center"
                            >
                              <div
                                class="flex items-center px-[24px] gap-[4px]"
                              >
                                <div
                                  class="text-white text-center font-plusJakartaSans lg:text-[14px] xl:text-[16px] not-italic font-bold lg:leading-[20px] xl:leading-[24px]"
                                >
                                  Admission
                                </div>
                              </div>
                            </div>

                            <div class="pt-[46px]">
                              <div
                                class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute"
                              >
                                <div class="absolute bottom-[6px] left-[4px]">
                                  <div
                                    class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                                  ></div>
                                </div>
                                <div class="absolute bottom-[6px] right-[4px]">
                                  <div
                                    class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                                  ></div>
                                </div>
                              </div>
                            </div>
                          </div>

                          <div
                            @click="makeCall()"
                            class="bg-color xl:h-[48px] md:h-[44px] h-[44px] relative animation cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                          >
                            <div class="absolute top-[6px] left-[6px]">
                              <div
                                class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                            <div class="absolute top-[6px] right-[6px]">
                              <div
                                class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                              ></div>
                            </div>
                            <div
                              class="absolute top-[6px] w-full flex justify-center"
                            >
                              <div
                                class="flex items-center py-[6px] px-[24px] gap-[4px]"
                              >
                                <div
                                  class="gradient-text text-center font-plusJakartaSans text-[16px] not-italic font-bold leading-[24px]"
                                >
                                  Contact Us
                                </div>
                              </div>
                            </div>

                            <div class="pt-[46px]">
                              <div
                                class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute rg-color"
                              >
                                <div class="absolute bottom-[6px] left-[4px]">
                                  <div
                                    class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                                  ></div>
                                </div>
                                <div class="absolute bottom-[6px] right-[4px]">
                                  <div
                                    class="h-[3px] w-[3px] button-border opacity-75 rounded-[1px]"
                                  ></div>
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
            </div>
          </div>
          <div
            class="flex items-center px-6 md:px-[80px] lg:px-10 xl:max-w-[1180px] xl:mx-auto xl:px-0 lg:pt-[60px] pt-[42px] fadeInUp"
          >
            <img
              src="https://em-content.zobj.net/source/apple/21/sparkles_2728.png"
              alt=""
              class="w-[18px] h-[18px] lg:w-[22px] lg:h-[22px]"
            />
            <div class="w-full h-[1px] mx-4 rounded bg-slate-200"></div>

            <img
              src="https://em-content.zobj.net/source/apple/21/sparkles_2728.png"
              alt=""
              class="w-[14px] h-[14px] lg:w-[18px] lg:h-[18px]"
            />
          </div>
          <div class="lg:pt-[28px] xl:pt-[28px] md:pb-0 md:pt-[28px] py-0">
            <div class="flex gap-[8px] px-[20px] md:px-[36px] fadeInUp">
              <div
                class="text-black font-plusJakartaSans not-italic font-bold text-[24px] leading-[32px] md:text-[30px] md:leading-[36px] lg:text-[30px] lg:leading-[36px] xl:text-[30px] xl:leading-[36px]"
              >
                Gardenia school
              </div>
              <div class="flex items-center">
                <img class="h-[38px] w-[38px]" src="/gardenia/sparkle.gif" />
              </div>
            </div>
            <div
              class="pt-[16px] px-[20px] md:px-[36px] md:pt-[16px] lg:pt-[20px] xl:pt-[20px] fadeInUp"
            >
              <div class="flex gap-[12px] flex-col">
                <div class="">
                  <span
                    class="text-neutral-500 font-plusJakartaSans text-[16px] not-italic leading-[24px] font-medium"
                  >
                    Gardenia – perceived as
                  </span>
                  <span
                    class="text-neutral-800 font-plusJakartaSans text-[16px] not-italic leading-[24px] font-semibold"
                  >
                    "A Hybrid Pearl of Education"
                  </span>
                  <span
                    class="text-neutral-500 font-plusJakartaSans text-[16px] not-italic leading-[24px] font-medium"
                  >
                    that blends Montessori Method with IGCSE Curriculum upto
                    12th Standard, is one of its kind.
                  </span>
                </div>
              </div>
            </div>

            <!-- large screen -->
            <div class="xl:px-0 lg:px-[32px] pt-[28px]">
              <div class="flex flex-col gap-[20px]">
                <div class="md:pb-[20px] lg:pb-[20px] pb-[20px] xl:pb-[20px]">
                  <div class="flex gap-[20px] overflow-hidden">
                    <div class="flex gap-[20px] slide-track fadeInUp">
                      <div
                        v-for="(slide, index) in slides"
                        :key="index"
                        class="w-[280px] gap-6 flex hover:scale-95 transition-transform transform duration-300 flex-col justify-between py-[20px] px-[20px] bg-white border border-slate-200 rounded-2xl"
                      >
                        <img class="h-[244px]" :src="slide.image" />
                      </div>
                    </div>
                    <div class="flex gap-[20px] slide-track">
                      <div
                        v-for="(slide, index) in slides"
                        :key="index"
                        class="w-[280px] gap-6 flex hover:scale-95 transition-transform transform duration-300 flex-col justify-between py-[20px] px-[20px] bg-white border border-slate-200 rounded-2xl"
                      >
                        <img class="h-[244px]" :src="slide.image" />
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div
            class="fadeInUp flex items-center px-6 md:px-[80px] lg:px-10 xl:max-w-[1180px] xl:mx-auto xl:px-0 lg:pt-[60px] pt-[42px]"
          >
            <img
              src="https://em-content.zobj.net/source/apple/21/sparkles_2728.png"
              alt=""
              class="w-[18px] h-[18px] lg:w-[22px] lg:h-[22px]"
            />
            <div class="w-full h-[1px] mx-4 rounded bg-slate-200"></div>

            <img
              src="https://em-content.zobj.net/source/apple/21/sparkles_2728.png"
              alt=""
              class="w-[14px] h-[14px] lg:w-[18px] lg:h-[18px]"
            />
          </div>
          <div class="pt-[48px] md:pt-[48px] lg:pt-[60px]">
            <div class="flex justify-center">
              <div
                class="border visitor-count-block max-w-[800px] w-full border-[#3B82F6] border-opacity-30 py-[36px] fadeInUp"
              >
                <div
                  class="flex items-center flex-col gap-[12px] justify-center"
                >
                  <div
                    class="h-[44px] w-[308px] border grid grid-cols-7 counter-box rounded-bl-[8px] rounded-[8px] bg-white border-neutral-200"
                  >
                    <div
                      v-for="(digit, index) in formattedVisitCount"
                      :key="index"
                      :class="{
                        'flex items-center justify-center border-r border-neutral-200':
                          index !== formattedVisitCount.length - 1,
                        'flex items-center justify-center':
                          index === formattedVisitCount.length - 1,
                      }"
                    >
                      <div
                        class="text-[18px] leading-[28px] font-medium not-italic font-plusJakartaSans text-center text-neutral-800"
                      >
                        {{ digit }}
                      </div>
                    </div>
                  </div>
                  <div
                    class="text-neutral-500 text-center font-plusJakartaSans not-italic text-[14px] font-medium leading-[20px]"
                  >
                    Total Visitors Sessions Optimized
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="xl:px-0 lg:px-[32px] pt-[28px]">
            <div
              class="fadeInUp pb-[48px] lg:pb-[60px] pt-[48px] md:pt-[60px] lg:pt-[48px] xl:pt-[60px] flex justify-center"
            >
              <div class="flex flex-col gap-[4px]">
                <div
                  class="text-black text-center items-center justify-center flex font-plusJakartaSans text-[24px] leading-[32px] xl:text-[30px] md:text-[30px] lg:text-[30px] not-italic font-bold md:leading-[36px] lg:leading-[36px] xl:leading-[36px]"
                >
                  Child's Work
                </div>
              </div>
            </div>
            <div class="flex flex-col gap-[20px]">
              <div class="md:pb-[20px] lg:pb-[20px] pb-[20px] xl:pb-[20px]">
                <div class="flex gap-[20px] overflow-hidden">
                  <div class="flex gap-[20px] slide-track fadeInUp">
                    <div
                      v-for="(img, index) in gallery"
                      :key="index"
                      class="w-[280px] gap-6 flex hover:scale-95 transition-transform transform duration-300 flex-col justify-between py-[20px] px-[20px] bg-white border border-slate-200 rounded-2xl"
                    >
                      <img class="h-[244px]" :src="img.image" />
                    </div>
                  </div>
                  <div class="flex gap-[20px] slide-track">
                    <div
                      v-for="(img, index) in gallery"
                      :key="index"
                      class="w-[280px] gap-6 flex hover:scale-95 transition-transform transform duration-300 flex-col justify-between py-[20px] px-[20px] bg-white border border-slate-200 rounded-2xl"
                    >
                      <img class="h-[244px]" :src="img.image" />
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="md:px-[36px] px-[20px]">
            <div
              class="fadeInUp pt-[48px] md:pt-[60px] lg:pt-[48px] xl:pt-[60px] flex justify-center"
            >
              <div class="flex flex-col gap-[4px]">
                <div
                  class="text-black text-center items-center justify-center flex font-plusJakartaSans text-[24px] leading-[32px] xl:text-[30px] md:text-[30px] lg:text-[30px] not-italic font-bold md:leading-[36px] lg:leading-[36px] xl:leading-[36px]"
                >
                  Montessori
                </div>
              </div>
            </div>
            <div class="block lg:block xl:hidden md:block">
              <div class="xl:px-0 lg:px-[32px]">
                <div class="flex flex-col gap-[20px]">
                  <div>
                    <main
                      class="grid md:grid-cols-2 grid-cols-1 gap-4 mt-6 md:mt-8 lg:mt-[52px] lg:gap-8 md:flex-row"
                    >
                      <div v-for="(item, index) in montessori" :key="index">
                        <div
                          class="fadeInUp group border-solid border-slate-200 shadow-[0px_1px_3px_0px_rgba(0,_0,_0,_0.1),_0px_1px_2px_-1px_rgba(0,_0,_0,_0.1)] h-[320px] xl:h-[349px] overflow-hidden bg-white flex flex-col border rounded-xl md:rounded-[20px]"
                        >
                          <img
                            :src="item.image"
                            class="transition-transform duration-300 group-hover:scale-105"
                          />
                          <div class="flex flex-col p-3 md:p-4 lg:p-6">
                            <h1
                              class="lg:text-lg text-base font-semibold leading-[28px] text-[#0f172a]"
                            >
                              {{ item.data }}
                            </h1>
                            <div class="flex flex-wrap gap-3 mt-3 lg:mt-[14px]">
                              <div
                                class="flex gap-[3px] md:gap-1 text-xs lg:text-[13px] leading-[20px] text-[#0f172a]"
                              >
                                {{ item.subtitle }}
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </main>
                  </div>
                  <div class="hidden lg:hidden xl:block md:hidden">
                    <main class="flex justify-center gap-4">
                      <div>
                        <div
                          class="fadeInUp group border-solid w-[370px] border-slate-200 shadow-[0px_1px_3px_0px_rgba(0,_0,_0,_0.1),_0px_1px_2px_-1px_rgba(0,_0,_0,_0.1)] overflow-hidden bg-white flex flex-col border rounded-xl md:rounded-[20px]"
                        >
                          <img
                            :src="montessori_1.image"
                            class="transition-transform duration-300 group-hover:scale-105"
                          />
                          <div class="flex flex-col p-3 md:p-4 lg:p-6">
                            <h1
                              class="lg:text-lg text-base font-semibold leading-[28px] text-[#0f172a]"
                            >
                              {{ montessori_1.data }}
                            </h1>
                            <div class="flex flex-wrap gap-3 mt-3 lg:mt-[14px]">
                              <div
                                class="flex gap-[3px] md:gap-1 text-xs lg:text-[13px] leading-[20px] text-[#0f172a]"
                              >
                                {{ montessori_1.subtitle }}
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </main>
                  </div>
                </div>
              </div>
            </div>
            <div class="hidden lg:hidden xl:block md:hidden">
              <div class="xl:px-0 lg:px-[32px]">
                <div class="flex flex-col gap-[20px]">
                  <div>
                    <main
                      class="grid md:grid-cols-2 xl:grid-cols-3 grid-cols-1 gap-4 mt-6 md:mt-8 lg:mt-[52px] lg:gap-8 md:flex-row"
                    >
                      <div v-for="(item, index) in montessori_2" :key="index">
                        <div
                          class="fadeInUp group border-solid border-slate-200 shadow-[0px_1px_3px_0px_rgba(0,_0,_0,_0.1),_0px_1px_2px_-1px_rgba(0,_0,_0,_0.1)] xl:h-[349px] overflow-hidden bg-white flex flex-col border rounded-xl md:rounded-[20px]"
                        >
                          <img
                            :src="item.image"
                            class="transition-transform duration-300 group-hover:scale-105"
                          />
                          <div class="flex flex-col p-3 md:p-4 lg:p-6">
                            <h1
                              class="lg:text-lg text-base font-semibold leading-[28px] text-[#0f172a]"
                            >
                              {{ item.data }}
                            </h1>
                            <div class="flex flex-wrap gap-3 mt-3 lg:mt-[14px]">
                              <div
                                class="flex gap-[3px] md:gap-1 text-xs lg:text-[13px] leading-[20px] text-[#0f172a]"
                              >
                                {{ item.subtitle }}
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </main>
                  </div>
                  <div class="hidden lg:block md:hidden">
                    <main class="flex justify-center gap-4">
                      <div>
                        <div
                          class="fadeInUp group border-solid w-[370px] border-slate-200 shadow-[0px_1px_3px_0px_rgba(0,_0,_0,_0.1),_0px_1px_2px_-1px_rgba(0,_0,_0,_0.1)] overflow-hidden bg-white flex flex-col border rounded-xl md:rounded-[20px]"
                        >
                          <img
                            :src="montessori_1.image"
                            class="transition-transform duration-300 group-hover:scale-105"
                          />
                          <div class="flex flex-col p-3 md:p-4 lg:p-6">
                            <h1
                              class="lg:text-lg text-base font-semibold leading-[28px] text-[#0f172a]"
                            >
                              {{ montessori_1.data }}
                            </h1>
                            <div class="flex flex-wrap gap-3 mt-3 lg:mt-[14px]">
                              <div
                                class="flex gap-[3px] md:gap-1 text-xs lg:text-[13px] leading-[20px] text-[#0f172a]"
                              >
                                {{ montessori_1.subtitle }}
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </main>
                  </div>
                </div>
              </div>
            </div>

            <div
              class="fadeInUp flex items-center px-6 md:px-[80px] lg:px-10 xl:max-w-[1180px] xl:mx-auto xl:px-0 lg:pt-[60px] pt-[42px]"
            >
              <img
                src="https://em-content.zobj.net/source/apple/21/sparkles_2728.png"
                alt=""
                class="w-[18px] h-[18px] lg:w-[22px] lg:h-[22px]"
              />
              <div class="w-full h-[1px] mx-4 rounded bg-slate-200"></div>

              <img
                src="https://em-content.zobj.net/source/apple/21/sparkles_2728.png"
                alt=""
                class="w-[14px] h-[14px] lg:w-[18px] lg:h-[18px]"
              />
            </div>
            <div
              class="fadeInUp pt-[48px] md:pt-[48px] lg:pt-[60px] xl:pt-[60px] max-w-[780px] flex justify-between"
            >
              <div class="flex flex-col gap-[4px]">
                <div
                  class="text-black font-plusJakartaSans text-[24px] leading-[32px] xl:text-[30px] md:text-[30px] lg:text-[30px] not-italic font-bold md:leading-[36px] lg:leading-[36px] xl:leading-[36px]"
                >
                  Montessori Education:
                  <span class="gradient-text">
                    From Infant-Toddler to Secondary
                  </span>
                </div>
              </div>
            </div>
            <div class="xl:px-0 lg:px-[32px]">
              <main
                class="grid pb-[48px] fadeInUp md:grid-cols-2 w-full xl:grid-cols-4 grid-cols-1 gap-4 mt-6 md:mt-8 lg:mt-[52px] lg:gap-8 md:flex-row"
              >
                <div
                  v-for="(item, index) in education"
                  :key="index"
                  class="flex flex-col transition-transform duration-300 hover:scale-105"
                >
                  <img
                    :src="item.img"
                    alt=""
                    class="lg:rounded-t-[30px] rounded-t-[20px] h-[240px] md:h-[300px] xl:h-[350px] object-cover"
                  />
                  <div
                    :style="{ backgroundColor: item.color }"
                    class="md:text-lg xl:text-2xl text-base font-black md:h-[108px] xl:h-[136px] p-5 md:p-6 xl:p-8 text-white lg:pb-12 pb-7 lg:pt-8 lg:rounded-b-[30px] rounded-b-[20px]"
                  >
                    {{ item.data }}
                  </div>
                </div>
              </main>
            </div>
            <div class="flex justify-center">
              <div
                class="text-black font-plusJakartaSans text-[24px] leading-[32px] xl:text-[30px] md:text-[30px] lg:text-[30px] not-italic font-bold md:leading-[36px] lg:leading-[36px] xl:leading-[36px]"
              >
                Location
              </div>
            </div>
            <div
              class="xl:pt-[60px] pt-[30px] md:pt-[48px] lg:pt-[48px] pb-[110px]"
            >
              <iframe
                src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d9571.804505164846!2d80.231115!3d12.87585!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3a525b9ab0ec6c93%3A0xb473715cbda8c402!2sGardenia%20Schools!5e1!3m2!1sen!2sus!4v1721824429058!5m2!1sen!2sus"
                class="w-full sm:w-[400px] md:w-[600px] lg:w-[800px] xl:w-[1100px] h-[300px] md:h-[450px] mx-auto border-0"
                allowfullscreen=""
                loading="lazy"
                referrerpolicy="no-referrer-when-downgrade"
              ></iframe>
            </div>
          </div>
        </div>

        <div
          class="fixed bottom-0 z-50 w-full border-t smooth backdrop-blur-lg lg:hidden border-slate-200"
        >
          <div class="grid gap-2">
            <div
              class="z-50 h-[78px] w-full rounded-lg flex justify-between gap-[12px] items-center py-[8px] md:px-[40px] px-[20px]"
            >
              <div class="w-[124px]">
                <div class="flex flex-col">
                  <div
                    class="text-neutral-800 font-plusJakartaSans text-[16px] font-bold leading-[24px]"
                  >
                    Start Enrolling
                  </div>
                  <div
                    class="text-neutral-800 font-plusJakartaSans text-[16px] font-bold leading-[24px]"
                  >
                    Today!
                  </div>
                </div>
              </div>
              <div>
                <div
                  @click="createAdmission()"
                  class="bg-gradient-to-l animation w-[184px] xl:h-[48px] md:h-[44px] h-[44px] from-[#06B6D4] to-[#22B2AA] relative cursor-pointer border border-opacity-40 border-[#22B2AA] pt-[2px] rounded-[8px]"
                >
                  <div class="absolute top-[6px] left-[6px]">
                    <div
                      class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                    ></div>
                  </div>
                  <div class="absolute top-[6px] right-[6px]">
                    <div
                      class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                    ></div>
                  </div>
                  <div class="absolute top-[10px] w-full flex justify-center">
                    <div class="flex items-center">
                      <div
                        class="text-white text-center font-plusJakartaSans text-[14px] not-italic font-bold leading-[20px]"
                      >
                        Admission
                      </div>
                    </div>
                  </div>

                  <div class="pt-[46px]">
                    <div
                      class="h-[20px] rounded-[6px] left-[2px] right-[2px] bottom-[2px] rounded-tr-none rounded-tl-none absolute"
                    >
                      <div class="absolute bottom-[6px] left-[4px]">
                        <div
                          class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                        ></div>
                      </div>
                      <div class="absolute bottom-[6px] right-[4px]">
                        <div
                          class="h-[3px] w-[3px] background opacity-75 rounded-[1px]"
                        ></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <transition v-if="admissionModel">
        <div
          class="fixed top-0 bottom-0 left-0 right-0 z-20 flex items-center content-center justify-center backdrop-blur-[8px] bg-black/75"
        >
          <div
            class="max-w-[800px] overflow-x-hidden h-[400px] md:h-auto md:w-[800px] w-[300px] p-8 mx-auto bg-white border border-gray-300 rounded-lg"
          >
            <h2 class="mb-6 text-2xl font-bold">Enquiry Form</h2>
            <form class="w-full">
              <div class="md:flex gap-[20px] w-full">
                <div class="w-full mb-4">
                  <label
                    for="childName"
                    class="block mb-2 font-bold text-gray-700"
                  >
                    Child's Name
                  </label>
                  <input
                    type="text"
                    id="childName"
                    v-model="enquiryForm.childName"
                    class="w-full px-3 py-2 border border-gray-300 rounded"
                    placeholder="Enter child's name"
                  />
                </div>
                <div class="w-full mb-4">
                  <label for="age" class="block mb-2 font-bold text-gray-700">
                    Age
                  </label>
                  <input
                    type="number"
                    id="age"
                    v-model="enquiryForm.age"
                    class="w-full px-3 py-2 border border-gray-300 rounded"
                    placeholder="Enter age"
                  />
                </div>
              </div>
              <div class="md:flex gap-[20px]">
                <div class="w-full mb-4">
                  <label
                    for="parentName"
                    class="block mb-2 font-bold text-gray-700"
                  >
                    Parent's Name
                  </label>
                  <input
                    type="text"
                    id="parentName"
                    v-model="enquiryForm.parentName"
                    class="w-full px-3 py-2 border border-gray-300 rounded"
                    placeholder="Enter parent's name"
                  />
                </div>
                <div class="w-full mb-4">
                  <label
                    for="contactNo"
                    class="block mb-2 font-bold text-gray-700"
                  >
                    Contact No
                  </label>
                  <input
                    type="text"
                    id="contactNo"
                    v-model="enquiryForm.contactNo"
                    class="w-full px-3 py-2 border border-gray-300 rounded"
                    placeholder="Enter contact number"
                  />
                </div>
              </div>
              <div class="md:flex gap-[20px]">
                <div class="w-full mb-4">
                  <label
                    for="locality"
                    class="block mb-2 font-bold text-gray-700"
                  >
                    Locality
                  </label>
                  <input
                    type="text"
                    id="locality"
                    v-model="enquiryForm.locality"
                    class="w-full px-3 py-2 border border-gray-300 rounded"
                    placeholder="Enter locality"
                  />
                </div>
                <div class="w-full mb-4">
                  <label
                    for="message"
                    class="block mb-2 font-bold text-gray-700"
                  >
                    Message
                  </label>
                  <textarea
                    id="message"
                    v-model="enquiryForm.message"
                    class="w-full px-3 py-2 border border-gray-300 rounded"
                    placeholder="Enter your message"
                  ></textarea>
                </div>
              </div>
              <div class="flex justify-between">
                <button
                  @click="submitForm()"
                  class="px-4 py-2 font-bold text-white bg-blue-500 rounded hover:bg-blue-700"
                >
                  Submit
                </button>
                <button
                  type="button"
                  class="px-4 py-2 font-bold text-white bg-gray-500 rounded hover:bg-gray-700"
                  @click="cancelForm()"
                >
                  Cancel
                </button>
              </div>
            </form>
          </div>
        </div>
      </transition>
    </div>
  </div>
</template>

<script setup>
useHead({
  script: [
    {
      src: "https://cdn.jsdelivr.net/npm/swiper/swiper-bundle.min.js",
    },
  ],
  link: [
    {
      rel: "stylesheet",
      href: "https://cdn.jsdelivr.net/npm/swiper/swiper-bundle.min.css",
    },
  ],
});
</script>
<script>
import { defineComponent } from "vue";
import AOS from "aos";
import "aos/dist/aos.css";
import Plyr from "plyr";

import "plyr/dist/plyr.css";

export default {
  data() {
    return {
      enquiryForm: {
        childName: "",
        age: null,
        parentName: "",
        contactNo: "",
        locality: "",
        message: "",
      },
      gallery: [
        {
          image: "https://gardeniaschools.com/images/school/school_2.jpeg",
        },
        {
          image: "https://gardeniaschools.com/images/new_pongal/pongal_15.jpeg",
        },
        {
          image: "https://gardeniaschools.com/images/activity/activity_6.jpeg",
        },
        {
          image: "https://gardeniaschools.com/images/activity/activity_1.jpeg",
        },
        {
          image: "https://gardeniaschools.com/images/activity/activity_5.jpeg",
        },
      ],
      visitCount: 0,
      admissionModel: false,
      form: {
        email: "",
        phone: "",
        fatherName: "",
        fatherOccupation: "",
        childName: "",
        childDOB: "",
        motherName: "",
        motherNumber: "",
        motherOccupation: "",
        location: "",
        availableTime: "",
      },
      education: [
        {
          img: "	https://gardeniaschools.com/images/upload/infant-toddler.jpg",
          color: "#0091C0",
          data: "Infant-Toddler (Ages 0-3):",
        },
        {
          img: "https://gardeniaschools.com/images/upload/primary.jpg",
          color: "#C24CB3",
          data: "Primary (Ages 3-6)",
        },
        {
          img: "https://gardeniaschools.com/images/upload/elementary.jpg",
          color: "#FF896C",

          data: "Elementary (Ages 6-12)",
        },
        {
          img: "	https://gardeniaschools.com/images/upload/secondary.jpg",
          color: "#178B13",

          data: "Secondary (Ages 12-18)",
        },
      ],
      texts: ["Scuola Montessori India"],
      displayText1: "",
      indices: [0, 0, 0],
      speed: 70,
      formattedDuration: "",

      montessori_1: {
        image:
          "https://images.squarespace-cdn.com/content/v1/50edad02e4b0829d0c4fd04e/1454704221682-IZ1GY16EMXDDGTI342PV/image-asset.jpeg?format=1000w",
        data: "MONTESSORI POWERED CHILDREN",
        subtitle: "Happy, Intellectual, Powerful and Future Ready Children",
      },
      montessori_2: [
        {
          image:
            "https://www.montessoridowntown.com/wp-content/uploads/10-Benefits-of-Montessori-Education-for-Your-Child.jpeg",
          data: "MONTESSORI POWERED SCHOOLING",
          subtitle: "The Schooling Redefined",
        },
        {
          image:
            "https://gardeniaschools.com/images/upload/Page%20Header%20Montessori%20Environment.jpg",
          data: "MONTESSORI POWERED SYSTEM",
          subtitle: "Montessori Power Unleashed",
        },
        {
          image:
            "https://gardeniaschools.com/images/upload/pageheader-upto12.jpg",
          data: "MONTESSORI POWERED CURRICULUM",
          subtitle: `Implementing Montessori Methodologies in Indian Boards' Curriculum`,
        },
      ],
      montessori: [
        {
          image:
            "https://www.montessoridowntown.com/wp-content/uploads/10-Benefits-of-Montessori-Education-for-Your-Child.jpeg",
          data: "MONTESSORI POWERED SCHOOLING",
          subtitle: "The Schooling Redefined",
        },
        {
          image:
            "https://gardeniaschools.com/images/upload/Page%20Header%20Montessori%20Environment.jpg",
          data: "MONTESSORI POWERED SYSTEM",
          subtitle: "Montessori Power Unleashed",
        },
        {
          image:
            "https://gardeniaschools.com/images/upload/pageheader-upto12.jpg",
          data: "MONTESSORI POWERED CURRICULUM",
          subtitle: `Implementing Montessori Methodologies in Indian Boards' Curriculum`,
        },
        {
          image:
            "https://images.squarespace-cdn.com/content/v1/50edad02e4b0829d0c4fd04e/1454704221682-IZ1GY16EMXDDGTI342PV/image-asset.jpeg?format=1000w",
          data: "MONTESSORI POWERED CHILDREN",
          subtitle: "Happy, Intellectual, Powerful and Future Ready Children",
        },
      ],

      slides: [
        {
          image:
            "	https://gardeniaschools.com/images/slider/gardeniaschools.jpg",
        },
        {
          image: "	https://gardeniaschools.com/images/slider/slider-half3.jpg",
        },
        {
          image: "	https://gardeniaschools.com/images/slider/slider-half4.jpg",
        },
        {
          image: "	https://gardeniaschools.com/images/slider/slider-half2.jpg",
        },
      ],
      images: [
        {
          src: "https://gardeniaschools.com/images/activity/activity_6.jpeg",
        },
        {
          src: "https://gardeniaschools.com/images/new_pongal/pongal_15.jpeg",
        },
        {
          src: "https://gardeniaschools.com/images/activity/activity_5.jpeg",
        },
      ],
    };
  },
  computed: {
    formattedVisitCount() {
      return this.visitCount.toString().padStart(7, "0").split("");
    },
  },
  mounted() {
    setTimeout(() => {
      this.admissionModel = true;
    }, 10000);
    this.getVisitCount("website1");
    this.typeWriter(0);
    document.body.style.overflow = "hidden";
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
  },

  methods: {
    imageClass(index) {
      if (index === 1) {
        return "w-64 h-64";
      } else {
        return "w-48 h-48";
      }
    },
    cancelForm() {
      this.admissionModel = false;
    },
    makeCall() {
      const phoneNumber = "+918248101180";

      window.location.href = `tel:${phoneNumber}`;
    },
    submitForm() {
      console.log("sd");
      this.$router.push({
        path: "/viewPage",
        query: {
          data: JSON.stringify(this.enquiryForm),
        },
      });
      this.admissionModel = false;
    },
    getVisitCount(siteKey) {
      let count = localStorage.getItem(`page_view_${siteKey}`);
      if (count) {
        this.visitCount = Number(count) + 1;
        localStorage.setItem(`page_view_${siteKey}`, this.visitCount);
      } else {
        this.visitCount = 1;
        localStorage.setItem(`page_view_${siteKey}`, this.visitCount);
      }
    },
    createAdmission() {
      this.admissionModel = true;
    },
    typeWriter(index) {
      setTimeout(() => {
        if (index < this.texts.length) {
          if (this.indices[index] < this.texts[index].length) {
            this[`displayText${index + 1}`] += this.texts[index].charAt(
              this.indices[index]
            );
            this.indices[index]++;
            setTimeout(() => this.typeWriter(index), this.speed);
          } else {
            this.typeWriter(index + 1);
          }
        }
      }, 50);
    },

    formatNumber(number) {
      return number.toLocaleString();
    },
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Averia+Libre:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Averia+Sans+Libre:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Averia+Serif+Libre:ital,wght@0,300;0,400;0,700;1,300;1,400;1,700&family=Dancing+Script:wght@400..700&family=Elsie:wght@400;900&family=Mulish:ital,wght@0,200..1000;1,200..1000&family=Plus+Jakarta+Sans:ital,wght@0,200..800;1,200..800&family=Protest+Revolution&family=Protest+Riot&family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&family=Sixtyfour:BLED@0..100&family=UnifrakturMaguntia&display=swap");

.borderColor {
  border: 1px solid rgba(255, 255, 255, 0.28);
}

.background rect {
  fill: black;
  fill-opacity: 0.48;
  backdrop-filter: blur(4px);
}

.animation:active {
  transform: scale(0.95);
  transition: transform 0.2s ease-in;
}

.animation {
  transition: all 0.5s ease-in-out;
}
.gradient-text {
  background: linear-gradient(90deg, #22b2aa, #138b84);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.shadow {
  box-shadow: 0px 4px 20px 0px rgba(0, 0, 0, 0.06);
}
.bg-custom {
  border-radius: 8px;
  background: linear-gradient(
    90deg,
    rgba(245, 245, 245, 0.8) 0%,
    rgba(245, 245, 245, 0) 100%
  );
}
.background {
  background: rgba(255, 255, 255, 0.24);
}
.button-border {
  background: linear-gradient(
    90deg,
    rgba(59, 130, 246, 0.24) 0%,
    rgba(6, 182, 212, 0.24) 100%
  );
}

.bg-color {
  box-shadow: 0px 2px 0px 0px rgba(255, 255, 255, 0.12) inset;
  background: linear-gradient(
    90deg,
    rgba(59, 130, 246, 0.04) 0%,
    rgba(6, 182, 212, 0.04) 100%
  );
}
.blur-gradient {
  background: linear-gradient(180deg, rgba(255, 255, 255, 0) 0%, #fff 100%);
}

.custom-border {
  border-radius: 12px;
  border: 2px solid rgba(255, 255, 255, 0.16);
}
.border-custom {
  border: 1.4px solid rgba(229, 229, 229, 0.6);
}

.bg {
  background: rgba(0, 0, 0, 0.12);
}
.slide-track {
  animation: slide-scroll 90s linear infinite;
}
.reverse-slide {
  animation: slide-scroll-reverse 90s linear infinite;
}

.slides-track {
  animation: slide-scroll 30s linear infinite;
}

.block-track {
  animation: slide-scroll-reverse 30s linear infinite;
}

.controls-visible {
  controls: true;
}
.controls-visible::-webkit-media-controls {
  display: block !important;
}
.controls-visible::-webkit-media-controls-enclosure {
  display: block !important;
}
.bg-color {
  box-shadow: 0px 2px 0px 0px rgba(255, 255, 255, 0.12) inset;
  background: linear-gradient(
    90deg,
    rgba(59, 130, 246, 0.04) 0%,
    rgba(6, 182, 212, 0.04) 100%
  );
}
@keyframes slide-scroll-reverse {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}

.type-text {
  margin: 0 6px;
  display: inline-block;
}
.form-group {
  display: flex;
  flex-direction: column;
}
.visitor-count-block {
  background: linear-gradient(
    90deg,
    rgba(59, 130, 246, 0.12) 0%,
    rgba(6, 182, 212, 0.12) 100%
  );
}
.counter-box {
  box-shadow: 0px 1px 2px -1px rgba(0, 0, 0, 0.1),
    0px 1px 3px 0px rgba(0, 0, 0, 0.1);
  background-color: white;
}

.fadeInUp {
  opacity: 0;
  transform: translateY(50px);
  transition: opacity 0.8s ease-out, transform 0.8s ease-out;
}

.fadeInUp.active {
  opacity: 2;
  transform: translateY(0);
}
</style>
