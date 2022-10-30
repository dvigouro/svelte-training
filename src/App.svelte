<script>
  import TailwindCss from "./TailwindCSS.svelte";
  import SmearViewer from "./lib/SmearViewer.svelte";
  import SmearList from "./lib/SmearList.svelte";

  let currentSmear = "falciparum";

  function smearListMessage(event) {
    currentSmear = event.detail.text;
  }
</script>

<TailwindCss />

<main class="container">
  <SmearList on:message={smearListMessage} />
  <div>
    <h1 class="text-blue-200 text-3xl font-bold underline">Plasmodium View</h1>
    <SmearViewer smearName={currentSmear} />
  </div>
</main>

<style>
</style>
