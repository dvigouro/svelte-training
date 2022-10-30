<script>
  import { each } from "svelte/internal";
  import { data } from "../smears_store";
  import { createEventDispatcher } from "svelte";

  const dispatch = createEventDispatcher();

  function smearSelected(smear) {
    dispatch("message", {
      text: smear,
    });
  }
</script>

<ul>
  {#each Object.keys($data) as smear}
    <li
      class="text-blue-500"
      on:click={() => smearSelected(smear)}
      on:keydown={() => smearSelected(smear)}
    >
      {smear}
    </li>
  {/each}
</ul>

<style>
</style>
