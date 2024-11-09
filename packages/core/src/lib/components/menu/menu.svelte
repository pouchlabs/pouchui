<script lang="ts">
 let {children,direction="verticle",classes="",size="xs",responsive=false} =$props()
</script>
<ul class:lg:menu-horizontal={responsive === true} class="menu bg-base-100 menu-{direction} menu-{size} {classes}">
   {#if children}
     {@render children()}
   {/if}
</ul>
