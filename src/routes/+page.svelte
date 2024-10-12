<script lang="ts">
    import Upload from '$lib/components/Upload.svelte';
	import { LightSwitch } from '@skeletonlabs/skeleton';

    let fileExist : boolean = false;

    const fileUploadHandler = (file : FileList) => {
        fileExist = true;
    }
</script>

<div class="flex flex-col w-screen h-screen">
    <div class="flex justify-start p-4">
        <LightSwitch />
    </div>
    { #if !fileExist }
    <div class="flex-grow flex justify-center items-center w-screen">
        <Upload fileHandler={fileUploadHandler} />
    </div>
    { /if }
</div>