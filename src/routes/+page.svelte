<script>
  import { gsap } from "gsap/dist/gsap";
  import { fly } from "svelte/transition";
  import { onMount } from "svelte";
  import { goto } from "$app/navigation";

  onMount(() => {
    const timeline = gsap.timeline();
    const h1Elements = document.querySelectorAll(".h1");
    // Loop through each h1 element and add animations to the timeline
    h1Elements.forEach((element) => {
      timeline.from(element, {
        opacity: 0,
        y: 20,
        duration: 0.5,
        delay: 0.5,
      });
    });

    timeline.to("#next-btn", {
      opacity: 1,
      y: -20,
      duration: 0.5,
      delay: 0.5,
    });
  });
</script>

<div
  out:fly={{ y: 200, duration: 500 }}
  class="container h-full mx-auto flex flex-col space-y-16 justify-center items-center"
>
  <div class=" flex flex-col items-center space-y-10">
    <h1 class="h1">DANCE YOUR WAY TO</h1>
    <h1 class="h1">SELF-DESCOVERY & FITNESS</h1>
    <h1 class="h1">WITH DANCE VERSE</h1>
  </div>
  <button
    id="next-btn"
    on:click={() => goto("/about")}
    class=" btn variant-filled btn-lg opacity-0">Start Journey</button
  >
</div>
