<script>
    import {AppBar} from '@skeletonlabs/skeleton';
    import digi_logo from '../../logos/logo.png';
    import { Avatar } from '@skeletonlabs/skeleton';
</script>

<AppBar>
    <svelte:fragment slot="lead">
        <strong class="ml-10">DIGISCOPE</strong>
    </svelte:fragment>
    <svelte:fragment slot="trail">
        <a class='btn bg-violet-600' href="/profile">
            <span><Avatar src="https://source.unsplash.com/YOErFW8AfkI/128x128" width="w-12" rounded="rounded-full" /></span>
            <span><strong>Jasmine</strong></span>
        </a> 
    </svelte:fragment>
</AppBar>