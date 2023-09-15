<script lang="ts">
  import { goto } from "$app/navigation";
  import { fade } from "svelte/transition";
</script>

<div
  transition:fade={{ duration: 300 }}
  class=" p-0 h-full flex flex-col items-center m-0 overflow-y-scroll"
>
  <div class=" w-[1000px] max-w-2xl flex flex-col m-16 space-y-4">
    <h1 class="h1">Dance Verse</h1>
    <hr />
    <h2 class="h2">Introduction</h2>
    <p>
      Dance Verse seeks to unlock the vibrant world of break dance and bring it
      to the forefront for high school and college students. This interactive
      multimedia project will shine a light on an art form that has remained
      under the radar, and will use real experiences to resonate with a younger
      generation.
    </p>
    <hr />

    <h2 class="h2">Background and Motivation</h2>
    <p>
      Break dancing, often simply called "breaking", is more than just a dance
      form. It is a language of movement, an expression of youth, and a bridge
      to cultures. I have been deeply passionate about break dancing since my
      high school days. This form of art has not only allowed me to escape the
      pressures of academia but has also gifted me with invaluable friendships
      and unforgettable experiences. As the leader of my break dance club in
      both high school and college, I was fortunate to perform and compete on
      various platforms. These memories remain some of the brightest highlights
      of my youth.
    </p>
    <p>
      The captivating world of break dance is still largely hidden from the
      general populace. It pains me to notice that many events related to this
      art are mainly attended by fellow dancers. The general public, especially
      the younger generation, remains largely oblivious to this vibrant culture
      and its benefits. Through this project, I hope to change that. I envision
      a multimedia production that showcases the world of break dance, making it
      accessible and appealing to high school and college students.
    </p>
    <hr />

    <h2 class="h2">Project Goals</h2>
    <ol class="list">
      <li>
        <span>1.</span>
        <span
          >Educate the young audience about the history and evolution of break
          dance.</span
        >
      </li>
      <li>
        <span>2. </span>
        <span
          >Highlight the physical and social benefits of engaging in break
          dancing.</span
        >
      </li>
      <li>
        <span>3. </span>
        <span
          >Encourage more students to explore break dance as a hobby or even a
          potential career.</span
        >
      </li>
    </ol>
    <hr />

    <h2 class="h2">Target Audience</h2>
    <p>High school and college students, especially those who:</p>
    <ol class="list">
      <li>
        <span>1. </span><span
          >Are seeking a medium of self-expression and physical activity.</span
        >
      </li>
      <li>
        <span>2. </span><span
          >Are curious about different art forms and cultures.</span
        >
      </li>
      <li>
        <span>3. </span>
        <span>
          Might be interested in dance but have little to no knowledge about
          break dance.</span
        >
      </li>
    </ol>
    <hr />

    <h2 class="h2">Design Considerations and Aspects</h2>
    <ol class="list">
      <li>
        <span>1. </span>
        <span>
          <b>Engaging Visuals:</b>Utilizing dynamic shots of break dance
          performances to grab the audience's attention.</span
        >
      </li>

      <li>
        <span>2. </span>
        <span>
          <b>Mobile Compatibility:</b>Ensuring that the multimedia production is
          mobile-friendly, as most high school and college students access
          content on their smartphones.</span
        >
      </li>
      <li>
        <span>3. </span>
        <span>
          <b>Accessible Language:</b>Keeping the content jargon-free, using
          simple and straightforward language to cater to our target audience.</span
        >
      </li>
    </ol>
    <p>
      By the end of this project, I aim to create a bridge between the
      mesmerizing world of break dance and young individuals looking for a
      medium of expression, fitness, and camaraderie. It is not just about
      promoting a dance form; it's about sharing a culture and lifestyle that
      has enriched countless lives, including my own.
    </p>

    <div class=" w-full flex items-center justify-center py-16">
      <button
        class="btn variant-filled btn-lg px-24"
        on:click={() => goto("/gallery")}>Check out Gallery!</button
      >
    </div>
  </div>
</div>
