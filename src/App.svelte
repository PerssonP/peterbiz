<script lang="ts">
  import malmofoodsImg from './assets/malmofoods.png';
</script>

<main>
  <a href="https://aquifer.peter.biz" class="wrapper">
    <div class="slide" id="aquifier">
      <p>Twitch aquifier</p>
    </div>
  </a>
  <a href="https://malmofoods.peter.biz" class="wrapper">
    <div class="slide">
      <img src={malmofoodsImg} />
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
  main {
    overflow: hidden;
  }

  .slide {
    position: relative;
    height: 150px;
    z-index: 2;

    background-color: rgb(0, 0, 0);
  }

  .slide::before {
    position: absolute;
    transform: skewx(-15deg);
    background-color: rgb(117, 93, 93);
    content: '';
    height: 100%;
    width: calc(100% + 40px);
    left: -20px;
    z-index: -1;

    transition: 0.25s;
  }

  .wrapper img {
    position: absolute;
    height: 100%;
    width: 100%;
    object-fit: scale-down;
    object-position: left;
    -webkit-mask-image: linear-gradient(to right, rgba(0, 0, 0, 1) 10%, transparent 50%);
    mask-image: linear-gradient(to right, rgba(0, 0, 0, 1) 10%, transparent 50%);
    left: 0px;
    transition: 0.25s;
  }

  .wrapper:hover .slide::before {
    left: -500px;
  }

  .slide p {
    position: absolute;
    z-index: 2;
    margin: 0;
    left: 50%;
    top: 50%;
  }
</style>
