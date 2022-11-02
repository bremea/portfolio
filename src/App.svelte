<script lang="ts">
  import Background from "./components/Background.svelte";
  import Tailwindcss from "./Tailwindcss.svelte";
</script>

<Tailwindcss />

<main class="w-full">
  <Background />

  <section class="w-full px-24 py-16">
    <p class="text-white">Brett Meadows</p>
    <p>Full-stack developer and student</p>
	<a href="mailto:brett@bremea.com" class="underline">brett@bremea.com</a>

	<p class="mt-12">Skills</p>
	<ul class="list-disc list-inside">
		<li>TypeScript</li>
		<li>C</li>
		<li>Java</li>
		<li>SQL</li>
		<li>Cassandra</li>
		<li>MongoDB</li>
		<li>Redis</li>
		<li>Node</li>
		<li>Next.js</li>
		<li>Unity</li>
		<li>Flutter</li>
		<li>GCP</li>
	</ul>

	<p class="mt-12">Projects</p>
	<ul class="list-disc list-inside">
		<li>Crowd Labs</li>
		<li>News App</li>
		<li>JTML</li>
		<li>GDraw</li>
	</ul>
  </section>
</main>
