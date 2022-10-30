<script>
  import SmearImage from "./SmearImage.svelte";
  import { data } from "../smears_store";

  export let smearName;

  let imageIndex = 0;

  function moveBack() {
    if (imageIndex > 0) {
      imageIndex -= 1;
    }
  }

  function moveForward() {
    if (imageIndex < $data[smearName].length - 1) {
      imageIndex += 1;
    }
  }

  $: if (smearName) {
    imageIndex = 0;
  }
</script>

<div class="flex flex-row border-l-pink-200">
  <div class="grow w-10 bg-slate-300">
    {#if imageIndex != 0}
      <div on:click={() => moveBack} on:keydown={() => moveBack}>Back</div>
    {/if}
  </div>
  <SmearImage {smearName} imageName={$data[smearName][imageIndex]} />
  <div class="grow w-10 bg-slate-300">
    {#if imageIndex < $data[smearName].length - 1}
      <div
        class="grow w-10"
        on:click={() => moveForward}
        on:keydown={() => moveForward}
      >
        Forward
      </div>
    {/if}
  </div>
</div>

<style>
</style>
