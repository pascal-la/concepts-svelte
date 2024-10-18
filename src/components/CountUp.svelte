<!-- import { useEffect, useState } from "react";

type CountUpProps = {
  from?: number;
  to: number;
  durationInSeconds?: number;
  className?: string;
};

const INTERVAL_TIME = 10;

const CountUp = ({
  from = 0,
  to,
  durationInSeconds = 3,
  className,
}: CountUpProps) => {
  const [count, setCount] = useState<number>(from);

  const duration = durationInSeconds * 1000;

  const step = ((to - from) * INTERVAL_TIME) / duration;

  useEffect(() => {
    const interval = setInterval(() => {
      setCount((prev) => {
        if (prev + step < to) return prev + step;
        clearInterval(interval);
        return to;
      });
    }, INTERVAL_TIME);

    return () => clearInterval(interval);
  }, [to, step]);

  return <span className={className}>{Math.round(count)}</span>;
};

export default CountUp; -->

<script>
  export let from;
  export let to;
  export let durationInSeconds;

  const countUp = 0;

</script>

<span class="text-red-500">
  {from} {to} {durationInSeconds}
</span>