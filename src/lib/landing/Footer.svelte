<script>
  const filenames = ['discord','linked','reddit']
  let type = 'color'

  const images = Array(3).fill(0).map((n,i)=>`/src/logos/social/${filenames[i]}-${type}.svg`)

</script>

<footer class="bg-neutral-100 text-center text-neutral-600 dark:bg-neutral-600 h-100 dark:text-neutral-200 ">
  <div class="flex items-center justify-center border-b-2 border-neutral-200 p-6 dark:border-neutral-500 ">
      <div class="flex justify-center items-center">
        {#each images as image}
          <a href="#!" class="mr-6 text-neutral-600 dark:text-neutral-200">
            <object data="{image}" title="nill" type="image/svg+xml" width="40px"> </object> 
          </a>
        {/each}
      </div>
  </div>

  <!--Copyright section-->
  <div class="bg-neutral-200 p-6 text-center dark:bg-neutral-700">
    <span>© 2023 Copyright</span>
    <br>
    <a class="font-semibold text-neutral-600 dark:text-neutral-400" href="https://github.com/ryulabs">Ryu Labs 🐲</a>
  </div>
</footer>