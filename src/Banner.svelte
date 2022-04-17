<script>
	import { slide } from 'svelte/transition';  

    let isActive = true;

    function show() {
            isActive = !isActive;
            }
</script>

<main>
    {#if isActive === true}
        <div  transition:slide|local >
            <h1 class="splash">
                NEW!
            </h1>
            <pre>
                ^
                | \
            |  \
            |   \
            |-----------------------------|
                |	 			  |
                |	 COFFEE BREAK FROM 9 - 5   |
            | 	DO NOT DISTURB           |
            |			             |
            -----------------------------
                
                
            </pre>
        
            <h1 class="exit" on:click={show}>
                X
            </h1>
        </div>
        {:else}
        <div class="hiddenbanner" on:click={show}  transition:slide|local>
            <p> click to show banner again</p>
        </div>
        {/if}
    
</main>

<style>
    .hiddenbanner{
        line-height: 24px;
    }
    .splash{
        z-index:1;
        position:absolute;
        left:50px;
        top:10px;
        transform: rotate(330deg);
    }
    .exit{
        z-index:1;
        position:absolute;
        right:50px;
        top:10px;
      
    }
    main{
        text-align: center;
    
        margin-top: 0px;
        padding-top: 0px;


          background:yellow;
          color:red;
          box-shadow: 10px 5px 5px rgba(22, 2, 2, .3);
    }
    pre{
        margin: 0;
        padding: 0;

    }

</style>