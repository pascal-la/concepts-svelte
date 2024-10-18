<script>
  export let from = 0;
  export let to;
  export let durationInSeconds = 3;
  export let classNames;

  const INTERVAL_TIME = 10;
  let count = 0;

  const duration = durationInSeconds * 1000;
  const step = ((to - from) * INTERVAL_TIME) / duration;

  const interval = setInterval(() => {
    if (count + step < to) return count = count + step;
    clearInterval(interval);
    return count = to;
  });
</script>

<span class={classNames}>{Math.round(count)}</span>