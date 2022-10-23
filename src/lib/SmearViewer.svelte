<script>
  import SmearImage from "./SmearImage.svelte";

  export let smearName;
</script>

<div class="row">
  <button>Back</button>
  <SmearImage {smearName} imageName={"pf220517213207.jpg"} />
  <button>Forward</button>
</div>

<style>
  .row {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: auto;
  }
</style>
