<script>
  export let secondsLeft = 0;
</script>

<progress id="progressBar" value={secondsLeft / 20 * 100} max="100"></progress>
