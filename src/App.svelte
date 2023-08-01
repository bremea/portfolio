<script lang="ts">
  import Background from "./components/Background.svelte";
  import Tailwindcss from "./Tailwindcss.svelte";

  let d = new Date(new Date().toLocaleString("en-US", { timeZone: "America/New_York" }));
  let hour = d.getHours().toString().padStart(2, "0");
  let minute = d.getMinutes().toString().padStart(2, "0");
  let second = d.getSeconds().toString().padStart(2, "0");

  let lineNums = Array.from({ length: 20 }, (_, i) => i + 1);

  setInterval(() => {
    d = new Date(new Date().toLocaleString("en-US", { timeZone: "America/New_York" }));
    hour = d.getHours().toString().padStart(2, "0");
    minute = d.getMinutes().toString().padStart(2, "0");
    second = d.getSeconds().toString().padStart(2, "0");
  }, 1000);
</script>

<Tailwindcss />

<main class="w-full">
  <Background />

  <section class="w-full min-h-screen flex items-center justify-center">
    <div class="text-center relative bg-black bg-opacity-50 backdrop-blur p-4 md:p-8 rounded-lg flex text-sm md:text-base shadow-md mx-4 md:mx-32">
      <div class="flex-col flex w-full">
        <p>
          <span class="font-black">bremea</span><br />
          hallo, welcome to my website.
        </p>
        <br />
        <p><span class="italic">it's <span class="font-black">{hour}:{minute}:{second}</span> in my timezone (GMT-5000)</span></p>
        <br />
        <p>
          <span class="font-black">socials: </span>
          <a href="https://github.com/bremea" target="_blank" rel="noreferrer" class="underline">github</a>,
		  <a href="mailto:jade@bremea.com" class="underline">email</a>,
          <a href="https://discord.com/users/710164635524923575" target="_blank" rel="noreferrer" class="underline">discord</a>
        </p>
      </div>
    </div>
  </section>
</main>
