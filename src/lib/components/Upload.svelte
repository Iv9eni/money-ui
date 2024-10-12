<script lang="ts">
    import { FileDropzone } from '@skeletonlabs/skeleton';
    import Icon from "@iconify/svelte";

    let file : FileList;
    export let fileHandler;

    const onChangeHandler = (e : Event) => {
        fileHandler(file);
    }
</script>

<FileDropzone class="w-[624px]" name="files" bind:files={file} on:change={onChangeHandler}>
	<div class="justify-center" slot="lead">
        <Icon class="text-5xl w-screen" icon="mdi:file-upload" />
    </div>
	<svelte:fragment slot="meta">
        Upload an Excel or CVS.
    </svelte:fragment>
</FileDropzone>