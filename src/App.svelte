<script>
  import SmearViewer from "./lib/SmearViewer.svelte";
  import SmearList from "./lib/SmearList.svelte";

  let currentSmear = "falciparum";

  function smearListMessage(event) {
    currentSmear = event.detail.text;
  }
</script>

<main>
  <SmearList on:message={smearListMessage} />
  <div>
    <h1>Plasmodium View</h1>
    <SmearViewer smearName={currentSmear} />
  </div>
</main>

<style>
</style>
