<script lang="ts">
let { children,sidebar,end=false} = $props();
</script>
<div class:drawer-end={end === true} class="drawer lg:drawer-open">
    <input id="main-layout" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content flex flex-col">
      <!-- Page content here -->
      <label for="main-layout"  class="btn fixed left-1 z-5 top-1  btn-ghost btn-circle btn-sm drawer-button lg:hidden">
        <svg
        xmlns="http://www.w3.org/2000/svg"
        class="h-5 w-5"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor">
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M4 6h16M4 12h16M4 18h7" />
      </svg>
      </label>
      <main class="w-full ml-10 lg:ml-0 p-1 h-full">
        {#if children}
        {@render children()}
      {/if}
      </main>
    
 
    </div>
    <div class="drawer-side">
      <label for="main-layout" aria-label="close sidebar" class="drawer-overlay"></label>
     
      <aside class="bg-base-200 z-10  text-base-content min-h-full w-80 p-2">
          {#if sidebar}
        {@render sidebar()}
        {/if}
      </aside>
    </div>
  </div>