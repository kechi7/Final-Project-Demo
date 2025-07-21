<script>
  let { title, subtitle } = $props();
</script>

<div class="title-card">
  <div class="content">
    <h1>{title}</h1>
    <p>{subtitle}</p>
  </div>
</div>

<style>
  /* * {
    height: 100vh;
    width: 100vh;
  } */


  .title-card {
    background-image: url("/Users/nkechi7/Final-Project-Demo/src/lib/Images/Main4.webp");
    /* Add the blur effect */

    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    /* padding: 2rem; */
    /* box-sizing: border-box; */
  }

  .content {
    background-color: rgb(0, 0, 0); /* Fallback color */
    background-color: rgba(0, 0, 0, 0.4); /* Black w/opacity/see-through */
    color: white;
    font-weight: bold;
    border: 3px solid #f1f1f1;
    position: absolute;
    padding: 10px;
    /* max-width: 700px;
    background-color: #034c36;
    padding: 2rem;
    border: 6px solid #e3ff00;
    border-radius: 2rem;
    box-shadow: 16px 16px #188f70; */
  }

  h1 {
    font-size: 4rem;
    margin: 0;
    color: #f1f1f1;
    text-shadow: 1px 1px 0 black;
  }

  p {
    font-size: 1.3rem;
    color: #f7f5eb;
    margin-top: 1rem;
  }

  @media (max-width: 600px) {
    h1 {
      font-size: 2.2rem;
    }

    p {
      font-size: 1.1rem;
    }
  }
</style>
