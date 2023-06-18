<script>
    import {AppBar} from '@skeletonlabs/skeleton';
    import digi_logo from '../../logos/logo.png';
    import { Avatar } from '@skeletonlabs/skeleton';
    import star_banner from '../../logos/star-banner.jpg';
</script>

<AppBar >
    <svelte:fragment slot="lead"> <img src="{digi_logo}" class="w-1/2"> </svelte:fragment>
    <svelte:fragment slot="trail">
        <a class='btn bg-violet-600' href="/profile">
            <span><Avatar src="https://source.unsplash.com/YOErFW8AfkI/128x128" width="w-12" rounded="rounded-full" /></span>
            <span><strong>Jasmine</strong></span>
        </a> 
    </svelte:fragment>
</AppBar>