<template>
  <!-- hero -->
  <section id="hero"
    class="items-center flex box-border pt-[50vw] md:px-[5.6rem] md:pt-[10vw]  md:pb-[100px] relative min-h-[75vh] md:min-h-[100vh] justify-start inspire"
  >
    <div class="max-w-full w-full md:max-w-[50%] md:w-[640px] text-left hero-container">
      <h1 class="text-center md:text-left ">
        <span
          class=" text-[32px] md:text-[44px] mt-[24px] mb-0 letter-spacing-[-.16px] text-white font-bold leading-tight"
        >
          Endless entertainment for all
        </span>
        <br />
        <span class="text-[16px] mt-[16px] md:text-[20px] mt-[24px] text-white leading-tight">
          <b>Bundle plans starting at $10.99/month</b>
        </span>
      </h1>
      <ul class="grid-list two-columns my-[18px]">
        <li class="grid-item justify-space-between">
          <div>
            <picture class="lg-200">
              <source
                media="(min-width: 1025px)"
                srcset="
                  //cnbl-cdn.bamgrid.com/assets/0a177d01b8c714142b33bf4c60130680e656a476328cb3f9dde997263aa7cedf/original
                "
                width="4584"
                height="1350"
              />
              <img
                src="//cnbl-cdn.bamgrid.com/assets/0a177d01b8c714142b33bf4c60130680e656a476328cb3f9dde997263aa7cedf/original"
                width="4584"
                height="1350"
                alt="Disney+ hulu"
              />
            </picture>
            <p>
              <span class="text-[16px]">Starting at </span>
              <span class="text-[20px] text-white font-bold">$10.99</span>
              <span class="text-[16px]">/mo.</span>
            </p>
          </div>
          <div class="">
            <ULink
              inactive-class="primary-blue"
              to="https://www.disneyplus.com/identity/sign-up/enter-email?pref=disney_bundle_duo_basic"
              >Select</ULink
            >
          </div>
        </li>
        <li class="grid-item justify-space-between">
          <div>
            <picture class="max-w-[400px] w-full">
              <source
                media="(min-width: 1025px)"
                srcset="
                  //cnbl-cdn.bamgrid.com/assets/e7398ed4ffc16eb4eca63f549664da62cda5e6c172d799d7619f9609eac3df71/original
                "
                width="711"
                height="128"
              />
              <img
                src="//cnbl-cdn.bamgrid.com/assets/e7398ed4ffc16eb4eca63f549664da62cda5e6c172d799d7619f9609eac3df71/original"
                width="711"
                height="128"
                alt="Max Bundle Logo"
              />
            </picture>
            <p>
              <span class="text-[16px]">Starting at </span>
              <span class="text-[20px] text-white font-bold">$10.99</span>
              <span class="text-[16px]">/mo.</span>
            </p>
          </div>

          <div class="">
            <ULink
              inactive-class="primary-blue"
              to="https://www.disneyplus.com/welcome/disney-hulu-max-bundle"
              >Select</ULink
            >
          </div>
          <div class="spacer"</div>
          <ULink
            to="https://www.disneyplus.com/welcome/disney-hulu-max-bundle"
            inactive-class="text-[12px] decoration-solid underline text-white"

            >Terms apply</ULink
          >
        </li>
      </ul>
      <div>
        <p class="mt-[24px] text-[12px]">
          <span class="">
            U.S. residents, 18+ only. Offer valid for eligible subscribers only. Select Hulu content available via Disney+ with valid Hulu and Disney+ subscriptions; additional content only available via Hulu app. © 2024 Disney and its related entities. 
          </span>
          <span class="">
            <!-- modal -->
            <ULink inactive-class="text-white underline decoration-solid "><span>Additional terms apply</span></ULink>
          </span>
          <span class="">.</span>
        </p>
      </div>
      <div class="">
        <p class="mt-[24px]">
          <span class="text-[12px]">©2024 Disney and its related entities. Max ©2024 Home Box Office, Inc.</span>
          <br/>
          <br/>
          <span class="text-[16px]">All of these and more now streaming.</span>
        </p>
      </div>
      <div class="mt-[20px]"></div>
      <ULink 
      inactive-class="text-[18px] decoration-solid underline text-white"> View All Plan Options</ULink>
    </div>
    <div class="background-image">
      <div class="bg-image-container">
        <picture><source media="(max-width: 768px)" srcset="//cnbl-cdn.bamgrid.com/assets/919441fecb0f6551256fd329ac757e05a1f529958c3842760975b9c6b65937d8/original" width="2048" height="2732"><source media="(min-width: 769px) and (max-width: 1024px)" srcset="//cnbl-cdn.bamgrid.com/assets/919441fecb0f6551256fd329ac757e05a1f529958c3842760975b9c6b65937d8/original" width="2048" height="2732"><source media="(min-width: 1025px)" srcset="//cnbl-cdn.bamgrid.com/assets/429cc70ade4e3a13e1d7bc268c8f355f435f12ea66d391acb3ac2d89fd85d330/original" width="3840" height="1620"><img src="//cnbl-cdn.bamgrid.com/assets/919441fecb0f6551256fd329ac757e05a1f529958c3842760975b9c6b65937d8/original" width="2048" height="2732" alt="Disney+, Hulu, ESPN+"></picture>
      </div>
    </div>
  </section>
</template>
<style scoped>

</style>
