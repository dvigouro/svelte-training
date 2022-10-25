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

<div class="row">
  <div class="nav">
    {#if imageIndex != 0}
      <div on:click={() => moveBack} on:keydown={() => moveBack}>Back</div>
    {/if}
  </div>
  <SmearImage {smearName} imageName={$data[smearName][imageIndex]} />
  <div class="nav">
    {#if imageIndex < $data[smearName].length - 1}
      <div on:click={() => moveForward} on:keydown={() => moveForward}>
        Forward
      </div>
    {/if}
  </div>
</div>

<style>
  .row {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: auto;
  }

  .nav {
    width: 20px;
  }
</style>
