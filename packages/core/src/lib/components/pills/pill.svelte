<script lang="ts">
    let { children,start,logo,trail} = $props();
</script>
<div class="avatar">
    <div class="w-8 mx-1 my-2 rounded">
        {#if logo}
             {@render logo()}
        {/if}
    </div>
</div>
<ul class="mx-auto mt-2 relative w-full h-full">
       {#if start}
         {@render start()}
      {/if}
      {#if children}
          {@render children()}
      {/if}
      <div class="fixed bottom-0 z-2 h-[200px] w-[42px] bg-base-100">
        {#if trail}
           {@render trail()}
         {/if}
      </div>
  </ul>
