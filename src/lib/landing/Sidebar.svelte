<script >
    import { AppRail,AppRailTile} from '@skeletonlabs/skeleton';
    import { zip } from 'lodash';
//https://icons8.com/
    let tile_num=0;
    export let routes = Array(0).fill(0)

    export let  names = Array(0).fill(0)

    const imagepaths = routes.map(n=>`/src/logos/dashboard/${n}/${n}-sticker.png`)

    const indexs     = imagepaths.map((n,i)=>i)

    const sum        = zip(routes,  names, imagepaths,indexs);

</script>

<AppRail>
    {#each sum as [route,  name, imagepath,i]}
        <AppRailTile bind:group={tile_num} name="tile-{i+1}" value={{i}} class="mb-8 hover:bg-blue-500">
            <a href="/{route}" class="flex-col justify-center items-center">
                <img src="{imagepath}" alt="" width="45px"  class="ml-4">
                <!-- <object data="{imagepath}"  class="ml-4" title="{route}" type="image/svg+xml" width="50px"></object> (svg)-->
                <strong class="text-center">{name}</strong>
            </a>
        </AppRailTile>
    {/each}
</AppRail>
