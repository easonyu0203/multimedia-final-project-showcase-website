<script lang="ts">
  import "../app.postcss";
  import { AppShell, AppBar } from "@skeletonlabs/skeleton";
  import { setModeUserPrefers, setModeCurrent } from "@skeletonlabs/skeleton";
  import { onMount } from "svelte";
  import { gsap } from "gsap/dist/gsap";
  import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
  onMount(() => {
    setModeUserPrefers(true);
    setModeCurrent(true);
  });
</script>

<AppBar shadow="shadow-lg">
  <svelte:fragment slot="lead">
    <strong class="text-xl uppercase">DANCE VERCE</strong>
  </svelte:fragment>
  <svelte:fragment slot="trail">
    <a class="btn btn-sm variant-ghost-surface" href="/"> Home </a>
    <a class="btn btn-sm variant-ghost-surface" href="/about"> About </a>
    <a class="btn btn-sm variant-ghost-surface" href="/gallery"> Gallery </a>
  </svelte:fragment>
</AppBar>
<slot />

<!-- App Shell -->
<!-- <AppShell regionPage="p-10">
  <svelte:fragment slot="header">
    <AppBar shadow="shadow-lg">
      <svelte:fragment slot="lead">
        <strong class="text-xl uppercase">DANCE VERCE</strong>
      </svelte:fragment>
      <svelte:fragment slot="trail">
        <a class="btn btn-sm variant-ghost-surface" href="/"> Home </a>
        <a class="btn btn-sm variant-ghost-surface" href="/about"> About </a>
        <a class="btn btn-sm variant-ghost-surface" href="/gallery">
          Gallery
        </a>
      </svelte:fragment>
    </AppBar>
  </svelte:fragment>
  <slot />
  <div
    style="pointer-events: none;"
    class="w-screen h-screen flex items-center justify-center top-0 left-0 absolute"
  >
    <div class="img-bg w-1/2 aspect-square" />
  </div>
</AppShell> -->

<style lang="postcss">
  .img-bg {
    @apply absolute z-[-1] rounded-full blur-[50px] transition-all;
    animation: pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite,
      glow 5s linear infinite;
  }
  @keyframes glow {
    0% {
      @apply bg-primary-400/50;
    }
    33% {
      @apply bg-secondary-400/50;
    }
    66% {
      @apply bg-tertiary-400/50;
    }
    100% {
      @apply bg-primary-400/50;
    }
  }
  @keyframes pulse {
    50% {
      transform: scale(1.5);
    }
  }
</style>
