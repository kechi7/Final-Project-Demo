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
      { threshold: 0.8 } // Trigger when 80% of section is in viewport
    );

    if (element) observer.observe(element);

    return () => {
      if (element) observer.unobserve(element);
    };
  });

  
</script>

<section class="background-section" bind:this={element}>
  {#if visible}
    <div class="introtext">
        <h1 class= "intro"> Red Lining and Wealth Disparity: The gap persists — and grows</h1>
      <p class="intro" transition:fade={{ duration: 1500 }}>
         Today, Black families hold less than a fraction of the wealth of white families. This is not because of lack of talent or effort, but because the starting lines were never equal.
      </p>
      

<div>
    <p class="introBold" transition:fade={{ duration: 1600 }}>
        Red Lining is a historic barrier that has caused inequities in wealth for Black communities.
    </p>
</div>

    </div>
  {/if}
</section>

<section>
<div>
        <div class='tableauPlaceholder' id='viz1753151737869' style='position: relative'><noscript><a href='#'><img alt='SCF Time Series  ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;BW&#47;BWDC-AssetsDebt-SCFTimeSeries&#47;SCFTimeSeries&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='BWDC-AssetsDebt-SCFTimeSeries&#47;SCFTimeSeries' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;BW&#47;BWDC-AssetsDebt-SCFTimeSeries&#47;SCFTimeSeries&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en-US' /></object></div>                
        <script type='text/javascript'>      
        var divElement = document.getElementById('viz1753151737869');     
        var vizElement = divElement.getElementsByTagName('object')[0];   
        vizElement.style.width='1200px';vizElement.style.height='600px';  
        var scriptElement = document.createElement('script'); 
        scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js'; 
        vizElement.parentNode.insertBefore(scriptElement, vizElement);  
        </script>
</div>

<div class="BWDCFacts">
      <h3 class="bwdcPara"> The Numbers</h3>
      <p>
        According to the BWDC, the graph displaying the median total net worth for households by Race/Ethnicity, there is a significant gap between the average net worth of Black households across
 all education levels and genders. Even though there is an evident increase in net worth from 2007 to 2022, there is still an identifiable gap between minority households and white households, especially when comparing Black households to White households.<br>
 In the context of redlining, this data shows how longstanding systemic barriers make it harder for marginalized demographics to create wealth even after the policies are abolished.

        
      <br>
        Formerly redlined neighborhoods were deemed "hazardous" for mortgage lending and other investments, leading to decades of disinvestment in infrastructure, amenities, and overall neighborhood conditions. This lack of financial support created and perpetuated a cycle of economic disadvantage. These areas often have higher poverty rates and unemployment, directly impacting median household income levels.
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

.tableau-container {
    position: relative;
    width: 5000px;
    padding-bottom: 56.25%; /* 16:9 ratio */
    height: 0;
}
.tableau-container iframe {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    border: 0;
}
    
.BWDCFacts{
padding:40px;
font-size: 20px;


}

</style>



