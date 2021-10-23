<div class="container">
  <main><slot/></main>
  <img
    class="background"
    src="/images/world.svg"
    width="1920"
    height="1080"
    alt="World Map"
  />
  <img
    class="background noise"
    src="/images/noise.svg"
    width="1920"
    height="1080"
    alt="Noise"
  />
</div>

<style>
  .container {
    max-width: 36rem;
    width: 100%;
    margin: 3rem auto 6rem;
  }

  .background {
    top: 0;
    left: 0;
    object-fit: cover;
    position: fixed;
    height: 100vh;
    width: 100vw;
    overflow: hidden;
    z-index: -1;
  }

  .noise {
    opacity: 0.2;
  }
</style>
