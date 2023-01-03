<script lang="ts">
</script>

<main>
  <a href="https://aquifer.peter.biz" class="wrapper">
    <div class="slide">
      <p>Twitch aquifier</p>
    </div>
  </a>
  <a href="https://malmofoods.peter.biz" class="wrapper">
    <div class="slide">
      <p>Malmö Foods</p>
    </div>
  </a>
  <a href="https://mrtn.peter.biz" class="wrapper">
    <div class="slide">
      <p>mrtn</p>
    </div>
  </a>
</main>

<style>
  .slide {
    position: relative;
    height: 150px;
    z-index: 300;
  }

  .slide::before {
    position: absolute;
    transform: skewx(-15deg);
    background-color: rgb(117, 93, 93);
    content: '';
    height: 100%;
    width: calc(100% + 40px);
    left: -20px;
    z-index: 1;

    transition: 0.25s;
  }

  .slide::after {
    position: absolute;
    background-color: aqua;
    content: 'Arrow';
    z-index: 0;
    height: 100%;
    width: 100%;
  }

  .wrapper:hover .slide::before {
    transition: 0.25s;
    left: -500px;
  }

  .slide p {
    position: absolute;
    z-index: 2;
    margin: 0;
  }
</style>
