<script>
    import {ALL_VIDEOS} from './archive.svelte';
    import Video from './Video.svelte';
    let singleValue = null;
    let width=100;
</script>


<main style=" --vidwidth:{width}px;">
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
        <br>
      </div>

{#each ALL_VIDEOS as v}
 <Video  Width =100%, Vid={v}>

</Video>


<!-- svelte-ignore a11y-media-has-caption -->
<!-- <div>
<video id ={v.id} width=100% controls>
    <source src={v.link}>
        your browser does not support video tag, please visit {v.link}
    </video>
    <p>
        {v.title}, by {v.director}, {v.duration} long. 
    </p> <button>+</button>
</div> -->
{/each}
</main>

<style>

  main{
    list-style:none;
    display: grid;
   
    grid-template-columns: repeat(auto-fit, var(--vidwidth));
    grid-auto-rows: max-content;
    grid-gap: 10px;
}

</style>