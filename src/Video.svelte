<script context = 'module'>
    export let Width=320;
    export let Height=240; 
    export let Vid={};
    
    
</script>

<!-- svelte-ignore a11y-media-has-caption -->
<video width={Width} height={Height} controls>
    <source src={Vid.link}>
        your browser does not support video tag, please visit {Vid.link}
    </video>
    <p>
        {Vid.title}, by {Vid.director}, {Vid.duration} long. 
    </p>
<main>

</main>


<style>


</style>