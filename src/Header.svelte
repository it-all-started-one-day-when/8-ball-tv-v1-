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
    <img
            src="https://cdn.glitch.global/333f567d-27a7-460e-86b4-8ea506dd9e09/8balltv-logo1.png?v=1644513101139"
            width="50"
            alt="picture of 8ball tv logo"
          />
  </div>
 

<style>
    div{
        text-align: center;
    }
    .slidecontainer{
        display: flex;
        justify-content: space-around;
      
    }
</style>