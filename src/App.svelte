<script lang="ts">
  import Background from "./components/Background.svelte";
  import Tailwindcss from "./Tailwindcss.svelte";

  let d = new Date(
    new Date().toLocaleString("en-US", { timeZone: "America/New_York" })
  );
  let hour = d.getHours().toString().padStart(2, "0");
  let minute = d.getMinutes().toString().padStart(2, "0");
  let second = d.getSeconds().toString().padStart(2, "0");

  setInterval(() => {
    d = new Date(
      new Date().toLocaleString("en-US", { timeZone: "America/New_York" })
    );
    hour = d.getHours().toString().padStart(2, "0");
    minute = d.getMinutes().toString().padStart(2, "0");
    second = d.getSeconds().toString().padStart(2, "0");
  }, 1000);
</script>

<Tailwindcss />

<main class="w-full">
  <Background />

  <section class="w-full min-h-screen flex items-center justify-center">
    <div
      class="bg-white bg-opacity-50 backdrop-blur p-4 md:p-8 rounded-lg text-sm md:text-base shadow-md mx-4 md:mx-24"
    >
      <p class="text-black font-bold">Brett Meadows</p>
      <p>Full-stack developer and student</p>
      <p>
        <a href="mailto:brett@bremea.com" class="underline">brett@bremea.com</a>
        ({hour}:{minute}:{second})
      </p>
      <br />
      <p>
        <span class="font-bold">Skills</span> [ TypeScript, C, Java, SQL, Cassandra,
        MongoDB, Redis, Node, Next.js, Unity, Flutter, GCP ]
      </p>
      <p><span class="font-bold">Learning</span> [ Rust, Go ]</p>
      <br />
      <p>
        <span class="font-bold">Projects</span> [
        <a
          href="https://aionary.com"
          target="_blank"
          rel="noreferrer"
          class="underline">AIonary</a
        >, Combo.Bot, Ads but Better, Crowd Labs ]
      </p>
    </div>
  </section>
</main>
