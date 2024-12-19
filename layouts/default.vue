<template>
  <div>
    <aside class="relative w-full box-border">
      <ULink
        to="https://www.disneyplus.com/identity/sign-up/enter-email?pref=disney_bundle_trio_basic"
      >
        <ClientOnly>
          <picture>
          <source
            media="(max-width: 768px)"
            srcset="
              https://cnbl-cdn.bamgrid.com/assets/722f00462378b1872e351f76c9e686cb59db585cda535361bd21c9666648d9f0/original
            "
            width="768"
            height="212"
          />
          <source
            media="(min-width: 769px) and (max-width: 1024px)"
            srcset="
              https://cnbl-cdn.bamgrid.com/assets/17e364941fafb7dc7b72e467597584c2f82a897ac29ef9b82faf96e3eb93d2e6/original
            "
            width="1024"
            height="222"
          />
          <source
            media="(min-width: 1025px)"
            srcset="
              https://cnbl-cdn.bamgrid.com/assets/b21a9ea8b0d719fbdf90083b49ea7635ebdb995526032ea397cb217aad1a4651/original
            "
            width="2880"
            height="150"
          />
          <img
            src="https://cnbl-cdn.bamgrid.com/assets/b21a9ea8b0d719fbdf90083b49ea7635ebdb995526032ea397cb217aad1a4651/original"
            width="2880"
            height="150"
            alt="ESPN on Disney+"
            loading="lazy"
          />
        </picture>
        </ClientOnly>
      </ULink>
    </aside>
    <nav class="nav flex h-[70px] justify-end absolute w-full">
      <ul class="nav-static gap-[16px] flex flex-wrap">
        <li class="items-center flex gap-15 nav-item"></li>
        <li class="items-center flex gap-15 nav-item"></li>
        <li class="items-center flex gap-15 nav-item justify-end">
          <a
            href=""
            class="small btn-nav secondary secondary-dark"
            ><span>LOG IN</span></a
          >
        </li>
      </ul>
    </nav>
    <slot />
  </div>
</template>
