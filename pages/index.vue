<template>
  <main>
    <Home />
    <section class="py-[2.3vw] text-center text-white">
      <p class="text-[40px] font-bold">Disney+ is Your Streaming Home for the Holidays</p>
      <p class="mt-[24px] text-[12px]">Your favorites from Hulu included in the Disney+ app for Disney Bundle subscribers</p>
      <Slider 
      :sliders="holidaysStreaming"
      :items-per-slide="5.5"
    />
    </section>
    <section class="py-[2.3vw] text-center text-white">
      <p class="text-[40px] font-bold">Trending</p>
      <Slider 
      :sliders="holidaysStreaming"
      :items-per-slide="5.5"
    />
    </section>
  </main>
</template>
<script setup>
const holidaysStreaming = [
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/a9aa3a4ca60ba8ccd83926f1fab3043021ee9f0011c44edac076b4cd80c3af8e/original",
      
      alt: "The Santa Clause"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/1301dc0f479410f14d0a5be0ebece2e47a4e4a5b143f7db3831b195bbec9e5c6/original",
      alt:"Doctor Who"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/5e3218d3749a3a67a8c4d19ca65fd49118bed05aaa1195ae94879bdfadf15437/original",
      alt:"Cristmas story"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/ec822d3f28debe973c334c92a82a43a9d884ea60f7c25e35ebaa880e744a5913/original",
      alt:"elf"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/dc54cf5d0995d4778271d836fc80b0bb2b893dcf6c346b473029109818d387a4/original",
      alt:"The Polar Express"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/1f183a0602285d3e542d7cba08e62490b28d2e3d742b2106245ecf17f2fea6ef/original",
      alt:"Christmas with the Kranks"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/71cbfab699acd19bfa4e1850ea95213e617bf6ef9bc010d8c5615b1c75479616/original",
      alt:"National Lampoon's Christmas Vacation"
  },
  {
    image:
      "https://cnbl-cdn.bamgrid.com/assets/8576ab9100d117e675324e85ff1265cb75105603eb951d2e8f652fd54f35054c/original",
      alt:"Four Christmases"
  },
];

</script>
