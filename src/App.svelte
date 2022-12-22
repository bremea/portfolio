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
    <div class="relative bg-black bg-opacity-50 backdrop-blur p-4 md:p-8 rounded-lg flex text-sm md:text-base shadow-md mx-4 md:mx-32">
      <div class="flex-col flex w-full">
        <p>
          <span class="font-black">Brett Meadows</span><br />
          Full-stack developer and student<br /><a href="mailto:brett@bremea.com" class="underline">brett@bremea.com</a>
        </p>
        <br />
        <p><span class="italic">It's <span class="font-black">{hour}:{minute}:{second}</span> in my timezone (GMT-5000)</span></p>
        <br />
        <p><span class="font-black">Skills: </span>TypeScript, C, Java, SQL, Cassandra, Prisma, Redis, NodeJS, NextJS, Unity, HTML, Linux, Docker, Kubernetes, GitHub, GCP, Svelte</p>
        <br />
        <p><span class="font-black">Learning: </span>Rust, Go, Flutter, AWS, Godot</p>
        <br />
        <p>
          <span class="font-black">Projects: </span><br />
          <a href="https://aionary.com" target="_blank" rel="noreferrer" class="underline">AIonary</a> (<span class="italic">Pictionary with an AI</span>)<br />
          <a href="https://github.com/bremea/tinfoil" target="_blank" rel="noreferrer" class="underline">Tinfoil</a> (<span class="italic">Scalable Discord API Library</span>)<br />
          <a href="https://getcrowd.app" target="_blank" rel="noreferrer" class="underline">Crowd Labs</a> (<span class="italic">Foot traffic analytics w/ IoT</span>)<br />
        </p>
        <br />
        <p>
          <span class="font-black">Socials: </span>
          <a href="https://github.com/bremea" target="_blank" rel="noreferrer" class="underline">Github</a>,
          <a href="https://discord.com/users/710164635524923575" target="_blank" rel="noreferrer" class="underline">Discord</a>,
          <a href="https://twitter.com/brett_8975" target="_blank" rel="noreferrer" class="underline">Twitter</a>
        </p>
      </div>
    </div>
  </section>
</main>
