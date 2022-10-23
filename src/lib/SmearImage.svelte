<script>
  export let imageName;
  export let smearName;

  $: imagePath = "/public/smears/" + smearName + "/images/" + imageName;
</script>

<div>
  <img class="smearImage" src={imagePath} alt="" srcset="" />
</div>

<style>
  .smearImage {
    width: 100%;
    height: auto;
  }
</style>
