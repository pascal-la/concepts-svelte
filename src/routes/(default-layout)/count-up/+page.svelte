<script>
	import CountUp from "../../../components/CountUp.svelte";

  const stats = [
  {
    title: "Voluptatum",
    subtitle:
      "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatum dolorum placeat eius.",
    to: 456,
    duration: 1,
  },
  {
    title: "Dignissimos",
    subtitle:
      "Totam maiores autem voluptatum dolorum temporibus dignissimos beatae assumenda!",
    from: 100,
    to: 1200,
    duration: 2,
  },
  {
    title: "Tempora",
    subtitle:
      "Tempora repellat culpa minus vel numquam! Dignissimos, dicta consequuntur!",
    from: 10000,
    to: 147000,
  },
];
</script>

<div class="container m-auto">
  <div class="grid gap-5 mt-24 mb-12">
    <h1
      class="text-4xl font-bold text-center bg-gradient-to-r from-emerald-300 to-emerald-800 bg-clip-text text-transparent">
      Nos réalisations
    </h1>
    <p class="text-slate-400">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Pariatur
      voluptatem eius ullam corrupti, harum quisquam necessitatibus enim
      obcaecati perspiciatis reiciendis quidem odit illo tempore inventore
      explicabo accusamus laboriosam suscipit? Ratione!
    </p>
  </div>
  <div class="grid md:grid-cols-3 gap-8 md:gap-5">
    {#each stats as stat, i}
      <div>
        <div class="grid justify-center size-full p-3 gap-5 text-center">
          <div>
            <h2 class="mb-3 text-2xl text-emerald-500 font-bold">
              {stat.title}
            </h2>
            <p class="text-slate-400 italic">{stat.subtitle}</p>
          </div>
          <CountUp from={stat.from} to={stat.to} durationInSeconds={i + 1} classNames="flex justify-center items-end h-full text-3xl text-emerald-400 font-bold"  />
        </div>
      </div>
    {/each}
  </div>
</div>