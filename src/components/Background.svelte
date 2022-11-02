<script type="ts">
  import { onMount } from "svelte";

  let canvas;
  onMount(() => {
    const context = canvas.getContext("2d");
    let time = 0;

    const color = function (x, y, r, g, b) {
      context.fillStyle = `rgb(${r}, ${g}, ${b})`;
      context.fillRect(x, y, 10, 10);
    };

    const R = (x, y, time) => {
      return Math.floor(64 * Math.cos((x * x - y * y) / 300 + time));
    };
    const G = (x, y, time) => {
      return Math.floor(
          64 *
            Math.sin(
              (x * x * Math.cos(time / 4) + y * y * Math.sin(time / 3)) / 300
            )
      );
    };
    const B = (x, y, time) => {
      return Math.floor(
          64 *
            Math.sin(
              5 * Math.sin(time / 9) +
                ((x - 100) * (x - 100) + (y - 100) * (y - 100)) / 1100
            )
      );
    };

    const startAnimation = () => {
      for (let x = 0; x <= 30; x++) {
        for (let y = 0; y <= 30; y++) {
          color(x, y, R(x, y, time), G(x, y, time), B(x, y, time));
        }
      }
      time = time + 0.01;
      requestAnimationFrame(startAnimation);
    };

    startAnimation();
  });
</script>

<canvas
  id="canvas"
  width="32px"
  height="32px"
  class="w-full h-full fixed top-0 left-0"
  bind:this={canvas}
/>

<style>
	canvas {
		z-index: -5;
	}
</style>