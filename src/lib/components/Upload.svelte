<script lang="ts">
    import { FileDropzone } from '@skeletonlabs/skeleton';
    import Icon from "@iconify/svelte";

    let inFile : FileList;
    export let outFile : FileList;

    const onChangeHandler = (e : Event) : void => {
        console.log('file data:', e);
    }
</script>

<FileDropzone class="w-[624px]" name="files" bind:files={inFile} on:change={onChangeHandler}>
	<div class="justify-center" slot="lead">
        <Icon class="text-5xl w-screen" icon="mdi:file-upload" />
    </div>
	<svelte:fragment slot="meta">
        Upload an Excel or CVS.
    </svelte:fragment>
</FileDropzone>