<script>
import { onMount } from 'svelte';

import ProgressBar from './ProgressBar.svelte';

let secondsLeft = 20;

function updateSecondsLeft() {
  setTimeout(() => {
    secondsLeft -= 1;
    secondsLeft === 0 ? alert('Time is up!') : updateSecondsLeft();
  }, 1000)
}

onMount(() => {
  updateSecondsLeft();
})
</script>

<h2>Seconds Left: {secondsLeft}</h2>
<ProgressBar {secondsLeft} />
