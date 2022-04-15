<script>
let width=100;
import {widthvar} from './stores.js'
function x(){
    widthvar.set(width)
};
let countvalue;
    widthvar.subscribe(value => {
        countvalue = value;
    });

</script>

<div class="slidecontainer">
    <input
      type="range"
      min="50"
      max="500"
      bind:value={width}
      class="slider"
      id="myRange"
      on:change={x}
    />
    <p>{countvalue}</p>
  </div>
 

<style>
    div{
        text-align: center;
    }
    .slidecontainer{
        margin-top: 30px;
    }
</style>