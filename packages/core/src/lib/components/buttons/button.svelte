<script lang="ts">
    import Loader from "../loaders/index.js";

    let {children,variant="",target="_self",size="",loader="ring",shape="",classes="",active=false,url="",disabled=false,outline=false,responsive=false,delay=3000} = $props()

    function asyncDelay(e){ 
    disabled=true;
    setTimeout(() => {
        disabled=false;
    },delay); 
}
</script> 

{#if responsive}
   {#if url}
   <a href="{url}" target="{target}" onclick={(e)=> asyncDelay(e)} class:btn-disabled={disabled === true} class:btn-active={active === true} class:btn-outline={outline === true} class="btn btn-{shape} btn-{size} btn-{variant} sm:btn-sm md:btn-md lg:btn-lg { classes } ">
    {#if disabled === true}
    <Loader type={loader} size={size} ></Loader>
    {:else}
    <div>
        {#if children}
          {@render children()}
        {/if}
     </div>
    {/if}
  
   </a>
   {:else}
   <button onclick={(e)=> asyncDelay(e)}  class:btn-active={active === true} class:btn-disabled={disabled === true} class:btn-outline={outline === true} class="btn btn-{shape} btn-{size} btn-{variant} sm:btn-sm md:btn-md lg:btn-lg {classes}">
    {#if disabled === true}
    <Loader type={loader} size={size} ></Loader>
    {:else}
    <div>
        {#if children}
          {@render children()}
        {/if}
     </div>
    {/if}
  
   </button>
  
   {/if}
  {:else}
   {#if url}
   <a href={url} target="{target}" onclick={(e)=> asyncDelay(e)}  class:btn-active={active === true} class:btn-disabled={disabled === true} class:btn-outline={outline === true} class="btn btn-{shape} btn-{size} btn-{variant} {classes}">
    {#if disabled === true}
    <Loader type={loader} size={size} ></Loader>
    {:else}
    <div>
        {#if children}
          {@render children()}
        {/if}
     </div>
    {/if}
  
   </a>
   {:else}
   <button onclick={(e)=> asyncDelay(e)}  class:btn-active={active === true} class:btn-disabled={disabled === true} class:btn-outline={outline === true} class="btn btn-{shape} btn-{size} btn-{variant} {classes}">
    {#if disabled === true}
   <Loader type={loader} size={size} ></Loader>
   {:else}
   <div>
       {#if children}
         {@render children()}
       {/if}
    </div>
   {/if}
 
</button>
   {/if}
 
{/if}


