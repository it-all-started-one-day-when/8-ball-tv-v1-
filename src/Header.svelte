<script>
let width=100;

</script>

<div class="slidecontainer">
    <input
      type="range"
      min="50"
      max="500"
      bind:value={width}
      class="slider"
      id="myRange"
    />
    <p>{width}</p>
  </div>
 

<style>
    div{
        text-align: center;
    }
    .slidecontainer{
        margin-top: 30px;
    }
</style>