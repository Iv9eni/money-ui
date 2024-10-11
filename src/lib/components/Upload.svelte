<script lang="ts">
    import { FileDropzone } from '@skeletonlabs/skeleton';
    import Icon from "@iconify/svelte";
</script>

<FileDropzone class="grid grid-cols-1 xl:grid-cols-1 gap-9 px-3 py-3" name="files">
	<div class="justify-center" slot="lead">
        <Icon class="text-4xl" icon="mdi:file-upload" />
    </div>
	<svelte:fragment slot="meta">
        Only CVS allowed.
    </svelte:fragment>
</FileDropzone>