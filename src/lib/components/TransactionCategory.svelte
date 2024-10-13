<script lang="ts">
<<<<<<< Updated upstream
    export let value;
</script>

<td>
    {value}
=======
    import { Autocomplete, popup } from "@skeletonlabs/skeleton";
    import type { AutocompleteOption, PopupSettings } from '@skeletonlabs/skeleton';

    export let value : string;
    let search : string = value;
    let isEditting : boolean = false;

    const categories: AutocompleteOption<string>[] = [
        {
            label: 'Car', value: 'car' 
        },
        {
            label: 'Entertainment', value: 'entertainment'
        },
        {
            label: 'Groceries', value: 'groceries'
        }
    ];

    let popupSettings: PopupSettings = {
        event: 'focus-click',
        target: 'popupAutocomplete',
        placement: 'bottom',
    };
    
    const onCategorySelection = (e: CustomEvent<AutocompleteOption<string>>): void => {
        search = e.detail.label;
    }

</script>

<td on:click={() => isEditting = true} >
    {#if isEditting}
        <input
            class="input autocomplete"
            type="search"
            name="autocomplete-search"
            bind:value={search}
            placeholder="Search..."
            use:popup={popupSettings} />
        <div data-popup="popupAutocomplete" tabindex="-1">
            <Autocomplete
                bind:input={search}
                options={categories}
                on:selection={onCategorySelection} />
        </div>
    {:else}
        {search}
    {/if}
>>>>>>> Stashed changes
</td>