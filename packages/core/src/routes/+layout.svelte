<script lang="ts">
	import {Provider,Main,Lv1,Pill,Button,Menu,Dropdown,Tooltip,Toggle,Checkbox,Radio,Range} from "$lib";
	import Preview from "../internal/preview.svelte";
	let { children } = $props();

</script>
<Provider>
	<Main>
		{#snippet  sidebar() }
	
		 {/snippet} 
	
		{@render children()}
	
		  <Menu direction='verticle' classes="bg-base-100" >
			 
		  </Menu>
		  <Tooltip>
			j
		  </Tooltip>
		  <Toggle>

		  </Toggle>
		  <Checkbox>
			h
		  </Checkbox>
		  <Radio>

		  </Radio>
		  <Range onValue={(v)=>{console.log(v,"j")}}>

		  </Range>
	</Main>

	
	
</Provider>
