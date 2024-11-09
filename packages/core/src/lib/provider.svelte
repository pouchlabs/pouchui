<script lang="ts">
import "./index.css";
let {children} = $props()
</script>
{#if children}
  {@render children()}
{/if}

	
