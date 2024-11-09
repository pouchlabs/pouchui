<script lang="ts">
    let {open=false,delay=3000,size="",position="",toggle}=$props()
</script>
<div class:dropdown-open={open === true} class="dropdown">
    <div tabindex="0" role="button" class="m-1">
        {#if toggle}
           {#snippet toggle()}
               {@render toggle()}
           {/snippet}
        {/if}

    </div>
    <ul tabindex="0" class="dropdown-content menu bg-base-100 rounded-box z-[1] w-52 p-2 shadow">
      <li><a>Item 1</a></li>
      <li><a>Item 2</a></li>
    </ul>
  </div>