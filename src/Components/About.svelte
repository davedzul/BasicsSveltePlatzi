<script>
    import Button from "./Botton.svelte";
    let someText="Frontend Developer at AgileThought";
    let count = 0;
    let styles = {darkMode:false};

    function handleClick (){
        count +=1;
    }

    function toggle(){
        styles.darkMode= !styles.darkMode;
        window.document.body.classList.toggle("dark-mode");
    }

</script>

<style>
    p{
        color:var(--theme-color);    
    }
</style>

<div class="About">
    {#if !styles.darkMode}
        <p>{someText}</p>
    {:else}
    <p><span>Hello darkMode</span></p>
    {/if}
    <Button 
    text="Click" 
    count={count}
    on:click={handleClick}
    />
<Button text="DarkMode" on:click={toggle}/>

<!-- <button on:click={handleClick}>Click {count === 0 ? '' : count}</button>
<button on:click={toggle}>DarkMode</button> -->
</div>