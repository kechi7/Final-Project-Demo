<script>
  const redDef = [
    "1933: Creation of the Home Owners Loan Corporation (HOLC) ",
    'Mid-1930s: "HOLC makes Residential Security Maps, marking minority neighborhoods as "hazardous" (redlined)',
    "1940s-1950s: FHA and VA use redlining maps to deny mortgage insurance to minority neighborhoods",
    "1968: Fair Housing Act passes, makes housing discrimination illegal",
    "1970s-1980s: Studies reveal ongoing discrimination and economic decline in redlined areas",
  ];
</script>

<div class="container">
  <div class="timeline">
    <h2 class="redliningtitle">Key Dates</h2>
    <ul>
      {#each redDef as point}
        <li>{point}</li>
      {/each}
    </ul>
  </div>

  <div style="color: white;" class="scroller">
    <div>
      <h1>The wealth gap didn’t just happen. It was built.</h1>
      <p>
        The United States has a long history of systemic violence. Historically,
        we have implemented systems, such as slavery, in which human life has
        been reduced to economic gain. While it is evident that we continue to
        progress towards positive change as a society, one truth still remains:
        the divisive systems of the past are never fully abolished, yet have
        evolved to work in our current socioeconomic climate. Specifically,
        policies like redlining, which have stemmed from decades, have
        perpetuated unequal access to education, subsequent job discrimination,
        and exclusion from wealth-building tools like home ownership, and have
        systematically shut Black communities out of opportunities for
        generations.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="redliningDepth">1930s</h3>
      <p>
        Neighborhoods with predominantly Black, immigrant, or low-income
        populations are marked in red on these maps as "hazardous" or high-risk,
        a practice known as redlining. This leads banks and insurers to deny
        loans and services in these areas.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="redliningDepth">1933</h3>
      <p>
        Redlining becomes institutionalized as the Federal Housing
        Administration (FHA) and Veterans Administration (VA) use these maps to
        determine eligibility for mortgage insurance and loans, effectively
        restricting Black Americans and minorities from homeownership and wealth
        accumulation.
      </p>
      <p>
        White flight to suburbs accelerates, reinforced by federally backed
        loans that exclude minority neighborhoods.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="timeline-date">Mid-1930s</h3>
      <p class="timeline-summary">
        Neighborhoods with predominantly Black, immigrant, or low-income
        populations are marked in red on these maps as "hazardous" or high-risk,
        a practice known as redlining. This leads banks and insurers to deny
        loans and services in these areas.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="timeline-date">1940s - 1950s</h3>
      <p class="timeline-summary">
        Redlining becomes institutionalized as the Federal Housing
        Administration (FHA) and Veterans Administration (VA) use these maps to
        determine eligibility for mortgage insurance and loans, effectively
        restricting Black Americans and minorities from homeownership and wealth
        accumulation.
      </p>
      <p class="timeline-summary">
        White flight to suburbs accelerates, reinforced by federally backed
        loans that exclude minority neighborhoods.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="timeline-date">1968</h3>
      <p class="timeline-summary">
        The Fair Housing Act is passed as part of the Civil Rights Act,
        outlawing discrimination in housing based on race, color, religion, sex,
        or national origin. However, the legacy of redlining continues in
        practice and effects.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="timeline-date">1970s - 1980s</h3>
      <p class="timeline-summary">
        Studies and activists begin to expose ongoing discrimination and
        disinvestment in formerly redlined neighborhoods, linking redlining to
        urban decay, poverty, and racial segregation.
      </p>
    </div>
    <div class="timelineDepth">
      <h3 class="timeline-date">1990</h3>
      <p class="timeline-summary">
        The Home Mortgage Disclosure Act (HMDA) requires lenders to publicly
        report their mortgage lending patterns, making discriminatory practices
        more visible.
      </p>
    </div>
    <div class="timelineDepth">
      <h3 class="timeline-date">1992</h3>
      <p class="timeline-summary">
        The Community Reinvestment Act (CRA) encourages banks to meet the credit
        needs of all communities, including low- and moderate-income
        neighborhoods, as a response to redlining.
      </p>
    </div>

    <div class="timelineDepth">
      <h3 class="timeline-date">2010s - Present</h3>
      <p class="timeline-summary">
        Research using historical HOLC maps shows that redlining’s effects
        persist in economic disparities, home values, health outcomes, and
        educational opportunities.
      </p>
      <p class="timeline-summary">
        Cities and organizations work to address redlining’s legacy through
        equitable housing policies and community reinvestment initiatives.
      </p>
    </div>

    <div>
      <a href="https://www.npr.org/2017/05/03/526655831/a-forgotten-history-of-how-the-u-s-government-segregated-america" target="_blank">Learn More</a>
    </div>
  </div>
  
</div>

<style>
  .container {
    display: flex;
    height: 100vh;
    overflow: hidden;
  }

  .timeline {
    flex: 1;
    position: sticky;
    top: 0;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 2rem;
  }

  .timelineDepth {
    background-color: rgba(51, 47, 47, 0.569);
    border-radius: 10px;
    padding: 10px;
  }

  .timeline ul {
    list-style: none;
    padding: 0;
  }

  .timeline li {
    padding: 0.5rem 0;
    color: #333;
    font-weight: 500;
  }

  .scroller {
    flex: 2;
    height: 100vh;
    overflow-y: scroll;
    padding: 4rem 2rem;
    box-sizing: border-box;
    background-color: rgb(100, 9, 9);
  }

  .scroller section {
    margin-bottom: 50vh; /* Creates space between scroll items */
    max-width: 600px;
  }

  .scroller h3 {
    margin-bottom: 1rem;
  }

  .scroller p {
    line-height: 1.6;
  }


  a:link, a:visited {
  background-color: black;
  color: white;
  border: 2px solid rgba(233, 182, 27, 0.633);
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  margin: 10px;
}

a:hover, a:active {
  background-color: rgb(205, 9, 9);
  color: white;
}
</style>
