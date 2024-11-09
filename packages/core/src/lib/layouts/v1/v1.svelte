<script lang="ts">
    let { children,sidebar,pill,end=false} = $props();
    </script> 
    <div class="inline-flex w-full h-full">
        <div class="h-screen min-h-screen z-50 pt-10  lg:p-1 overflow-y-auto no-scrollbar  p-1 flex-shrink-0 flex-grow-0 block top-0 left-0 fixed min-w-[50px] w-[50px] s-lg bg-base-100">
           {#if pill}
             {@render pill()}
          {/if}
        </div>
        <div class:drawer-end={end === true} class="drawer lg:drawer-open">
            <input id="main-layout" type="checkbox" class="drawer-toggle" />
            <div class="drawer-content w-full flex flex-col">
              <!-- Page content here -->
              <label for="main-layout"  class="btn fixed sm:m-1 left-1 z-50 top-1  btn-ghost btn-circle btn-sm drawer-button lg:hidden">
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
              <main class="w-full ml-[50px] lg:ml-1 p-1 h-full">
                {#if children}
                {@render children()}
              {/if}
              </main>
            
         
            </div>
            <div class="drawer-side">
              <label for="main-layout" aria-label="close sidebar" class="drawer-overlay"></label>
             
              <aside class="bg-base-200  ml-[45px] lg:ml-[45px] text-base-content min-h-full w-80 p-4">
                  {#if sidebar}
                {@render sidebar()}
                {/if}
              </aside>
            </div>
          </div>
    </div>
  