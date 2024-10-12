<script lang="ts">
    import Upload from '$lib/components/Upload.svelte';
	import { LightSwitch } from '@skeletonlabs/skeleton';

    let new_file : File;
</script>

<div class="flex flex-col w-screen h-screen">
    <div class="flex justify-start p-4">
        <LightSwitch />
    </div>
    <div class="flex-grow flex justify-center items-center w-screen">
        <Upload />
    </div>
</div>