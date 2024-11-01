<script lang="ts">
let { children,sidebar} = $props();
</script>
<div class="drawer lg:drawer-open">
    <input id="main-layout" type="checkbox" class="drawer-toggle" />
    <div class="drawer-content flex flex-col items-center justify-center">
      <!-- Page content here -->
      <label for="main-layout" class="btn fixed left-1 z-50 top-1  btn-ghost btn-circle btn-sm drawer-button lg:hidden">
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
      {#if children}
        {@render children()}
      {/if}
 
    </div>
    <div class="drawer-side">
      <label for="main-layout" aria-label="close sidebar" class="drawer-overlay"></label>
      <aside class="bg-base-200 md:p-8 text-base-content min-h-full w-80 p-4">
          {@render sidebar()}
      </aside>
    </div>
  </div>