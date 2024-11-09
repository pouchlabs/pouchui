<script lang="ts">
    let {checked=false,variant="",size="",disabled=false,children,classes="",min=0,max=100,value=20,onValue=()=>{}}=$props();
    function handleChange(e){
       value=value
        if(onValue){
            if(typeof onValue === "function"){
               return onValue(value)
            }
        }
    }
</script>
<input type="range" onchange={(e)=>{handleChange(e)}} min={min} max={max} bind:value={value} checked={checked} disabled={disabled} class="range range-{variant} range-{size} {classes}" />
{@render children?.()}