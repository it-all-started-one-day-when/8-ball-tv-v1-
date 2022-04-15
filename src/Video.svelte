<script>
    export let Width;
    export let Height; 
    export let Vid;
    
    
</script>
<div>
<!-- svelte-ignore a11y-media-has-caption -->
<video width={Width} height={Height} controls>
    <source src={Vid.link}>
        your browser does not support video tag, please visit {Vid.link}
    </video>
    <p>
        {Vid.title}, by {Vid.director}, {Vid.duration} long. 
    </p>
</div>


<style>


</style>