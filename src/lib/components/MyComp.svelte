<script lang="ts">
	import { afterUpdate } from 'svelte';

	// your script goes here
	$: {
		console.log('in my component ' + JSON.stringify($$slots, null, 2));
	}

</script>

<div>
	<slot />
</div>
