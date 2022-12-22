<svelte:head>
  <meta name="viewport" content="width=device-width" />
  <meta content="bremea" property="og:title" />
  <meta
    content="Full-stack developer and student"
    property="og:description"
  />
  <meta content="https://bremea.com/" property="og:url" />
  <meta content="#4CC9F0" data-react-helmet="true" name="theme-color" />
</svelte:head>

<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  @import url("https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@100;300;400;500;700;800;900&display=swap");

  * {
    font-family: "JetBrains Mono", monospace;
    @apply text-white;
  }

  img {
	height: 100%;
  }
</style>
