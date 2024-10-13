<script lang="ts">
	import { Autocomplete } from "@skeletonlabs/skeleton";
    import type { AutocompleteOption } from '@skeletonlabs/skeleton';

    let isEditting : boolean = false;
    let search : string = '';

    export let value : string;
    export const categories : string[] = ['car'];
</script>

<td on:click={() => isEditting = !isEditting}>
    {#if isEditting}
        <Autocomplete allowlist={categories} />
    {:else}
        {value}
    {/if}
</td>