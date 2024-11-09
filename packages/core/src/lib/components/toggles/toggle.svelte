<script lang="ts">
 let {checked=false,variant="primary",size="",children,disabled=false,classes=""}=$props();
</script>
<input type="checkbox" class="toggle toggle-{variant} toggle-{size} {classes}" disabled={disabled} checked={checked} />
{@render children?.()}