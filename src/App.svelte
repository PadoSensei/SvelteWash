<script>
  import Timer from "./Timer.svelte";
  import HowTo from "./HowTo.svelte";
  let audio;
  function timerEnds(e) {
    audio.play();
  }
</script>

<style>
  h1,
  h3 {
    text-align: center;
  }
</style>

<body>
  <h1>HandWasher1000</h1>
  <Timer on:end={timerEnds} />
  <HowTo />

  <h3>
    <a href="https://www.who.int/gpsc/clean_hands_protection/en/">
      Picture Source
    </a>
    <a href="https://www.freesound.org/people/metrostock99/sounds/345086/">
      Sound Source
    </a>
  </h3>

  <audio bind:this={audio}>
    <source src="Oh Yeah.wav" />
  </audio>
</body>
