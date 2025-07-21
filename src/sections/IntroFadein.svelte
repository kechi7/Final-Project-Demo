<script>
  import { fade } from "svelte/transition";
  import { onMount } from "svelte";

  let visible = false;
  let element;

  onMount(() => {
    const observer = new IntersectionObserver(
      ([entry]) => {
        if (entry.isIntersecting) {
          visible = true;
        }
      },
      { threshold: 0.8 } // Trigger when 50% of section is in viewport
    );

    if (element) observer.observe(element);

    return () => {
      if (element) observer.unobserve(element);
    };
  });
</script>

<section class="background-section" bind:this={element}>
  <div class="blur-overlay"></div>
  {#if visible}
    <div class="introtext">
      <p class="intro" transition:fade={{ duration: 1500 }}>
        In America, wealth too often determines how we judge others' value: who
        we listen to, who we respect, and who we care about.
      </p>
      <p class="introBold" transition:fade={{ duration: 1600 }}>
        But wealth isn't just personal. It’s historical.
      </p>
    </div>
  {/if}
</section>

<style>
  .background-section {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: black;
    margin: 0;
    padding: 0;
  }

  .intro {
    text-align: center;
    max-width: 600px;
    padding: 2rem;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border-radius: 10px;
    font-size: 23px;
    line-height: 1.5;
  }
  .introBold {
    text-align: center;
    max-width: 600px;
    padding: 2rem;
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border-radius: 10px;
    font-size: 23px;
    line-height: 1.5;
    font-weight: 700;
  }
</style>
