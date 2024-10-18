<script>
  const links = [
    {
      name: "Home",
      path:"/"
    },
    {
      name: "Login",
      path:"/login"
    },
    {
      name: "Contact",
      path:"/contact"
    },
    {
      name: "CountUp",
      path:"/count-up"
    },
    {
      name: "Blog",
      path:"/blog"
    },
  ];
</script>

<header class="absolute top-0 left-0 right-0 flex items-center p-3 gap-3 bg-emerald-600 h-12">
  {#each links as link}
  <a href="{link.path}">{link.name}</a>
  {/each}
</header>