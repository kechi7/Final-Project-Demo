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
         When wealth becomes a proxy for worth, entire communities are dismissed.
 People with less are treated as less deserving of compassion, resources, and opportunities.
 But behind these numbers are real people, families, and futures.

      </p>
      <p class="introBold" transition:fade={{ duration: 1600 }}>
        When we measure worth by wealth, we all lose sight of our shared humanity.
      </p>
    </div>
  {/if}


  
</section>

<section class = "eqSec">
    <div class= "Equity1">
        <h3 class = "eqt"> The Future — Reclaiming the Narrative</h3>
        <p> History explains the gap. But action can close it. We can invest in our communities, in our efforts for equity, our collective struggle for justice by first challenging the narratives that tie the worth of our most vulnerable communities 
</p>
    </div>


    <div>
	<img class = "blk" src="https://www.pewresearch.org/wp-content/uploads/sites/20/2025/02/SR_25.02.12_black-owned-businesses_feature.jpg" alt="whatever">
<div class= "Equity1">
	<p class= "caption">Black Owned Bos.’s weekend market in Boston’s Seaport neighborhood on Sept. 22, 2024. (Jessica Rinaldi/The Boston Globe via Getty Images) </p>
</div>
	
</div>

    
<div class= "Equity1">
<p>
 According to the Pew Research Center, Black-owned firms experienced a substantial increase in gross revenue, rising by 66% from $127.9 billion in 2017 to $211.8 billion in 2022. 
    </p>
    </div>


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

  .eqSec {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 700px;
    margin: 5rem auto;
    padding: 3rem;
    gap: 2rem;
    background-color: #f8f8f8;
    border-radius: 12px;
}

.Equity1 {
    max-width: 600px;
    text-align: center;
    font-size: 1rem;
    line-height: 1.6;
}

.eqt {
    font-size: 1.5rem;
    margin-bottom: 1rem;
}

.blk {
    width: 100%;
    max-width: 400px;
    height: auto;
    border-radius: 8px;
}

.caption {
    font-size: 0.85rem;
    color: #555;
    margin-top: 0.5rem;
}

</style>
