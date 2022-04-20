<script>
    import {push, pop, replace} from 'svelte-spa-router';
    import Video from '../Video.svelte'
    import {ONE_VIDEO, ALL_VIDEOS, filterfunc} from '../archive.svelte';

   

    export let params = {};
    let v =filterfunc('30-tambellini');
    console.log(v);
    const go_back = () => {
        pop();
    }
</script>
<main>
    <h1>this is the video you clicked on</h1>

    <h2>video id: {params.id}</h2>
    <!-- <h2>this {v}</h2> -->
    <div class="vidbox">
        <Video  Width =100%, Vid={ONE_VIDEO}></Video>
    </div>
    
    <button on:click={(go_back)}>Back</button>

</main>

<style>
    .vidbox{
        margin:10vw;
        width:80vw;
    }

</style>