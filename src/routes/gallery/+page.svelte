<script lang="ts">
  import banner from "$lib/imgs/banner.png";
  import poster from "$lib/imgs/poster.png";
  import logo from "$lib/imgs/logo.png";
  import videoThumnail from "$lib/imgs/videoThumnail.png";
  import { fly, fade } from "svelte/transition";
  import { onMount } from "svelte";
  import { gsap } from "gsap";

  const data = {
    banner: {
      src: banner,
      alt: "banner",
      link: "/products/banner",
      header: "Dancer Verse Banner",
      subtitle: "Dance Verse welcome you",
    },
    poster: {
      src: poster,
      alt: "poster",
      link: "/products/poster",
      header: "Dance Verse Poster",
      subtitle: "Join us to build your strength and make friends!",
    },
    logo: {
      src: logo,
      alt: "logo",
      link: "products/logo",
      header: "Dance Verse Logo",
      subtitle: "A logo representing our love for break dance",
    },
    videoThumnail: {
      src: videoThumnail,
      alt: "video",
      link: "/products/video",
      header: "Welcoming Video",
      subtitle: "Don't know want break dance is? check out your video!",
    },
  };
</script>

<div
  class="  w-full h-full flex flex-col justify-start items-center space-y-24 overflow-y-scroll py-16"
>
  <div
    transition:fly={{ y: 200, duration: 500 }}
    id="img-section"
    class="w-full h-[70vh] flex flex-col justify-start items-center space-y-16"
  >
    <h1 class="h1">IMAGES</h1>
    <div class="w-full flex justify-center items-center space-x-10">
      {#each [data.banner, data.poster, data.logo] as product}
        <a href={product.link} class=" card card-hover max-w-sm rounded-xl">
          <section>
            <header>
              <img
                src={product.src}
                alt={product.alt}
                class="w-full rounded-t-xl aspect-[16/13] object-cover"
              />
            </header>
            <div class="p-4 space-y-2">
              <h3 class="h3" data-toc-ignore>{product.header}</h3>
              <h6 class="h6" data-toc-ignore>{product.subtitle}</h6>
            </div>
            <hr class="opacity-50" />
            <footer class="p-4 flex justify-start items-center space-x-4">
              <div class="flex-auto flex justify-between items-center">
                <h6 class="font-bold" data-toc-ignore>By Eason</h6>
                <small>On 10/09/2023</small>
              </div>
            </footer>
          </section>
        </a>
      {/each}
    </div>
  </div>

  <div
    transition:fly={{ y: 200, duration: 500 }}
    id="video-section"
    class=" flex flex-col justify-start items-center space-y-10 pb-24"
  >
    <h1 class="h1">VIDEO</h1>
    <div class="w-full flex justify-center items-center space-x-10">
      <a
        href={data.videoThumnail.link}
        class=" card card-hover max-w-sm rounded-xl"
      >
        <section>
          <header>
            <img
              src={data.videoThumnail.src}
              alt={data.videoThumnail.alt}
              class="w-full rounded-t-xl aspect-[16/9] object-fill"
            />
          </header>
          <div class="p-4 space-y-2">
            <h3 class="h3" data-toc-ignore>{data.videoThumnail.header}</h3>
            <h6 class="h6" data-toc-ignore>{data.videoThumnail.subtitle}</h6>
          </div>
          <hr class="opacity-50" />
          <footer class="p-4 flex justify-start items-center space-x-4">
            <div class="flex-auto flex justify-between items-center">
              <h6 class="font-bold" data-toc-ignore>By Eason</h6>
              <small>On 10/09/2023</small>
            </div>
          </footer>
        </section>
      </a>
    </div>
  </div>
</div>
