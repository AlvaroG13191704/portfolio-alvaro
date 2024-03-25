<script lang="ts">
  export let nameList: string[];
  export let title: string = "programming languages that I use daily";
  export let pre: string ="The";
</script>

<p class="text-base sm:text-lg md:text-xl">
  {pre} <span class="text-violet-400">{title}</span
  >
</p>
<div class="flex flex-row flex-wrap gap-4">
  {#each nameList as name}
    <span class="p-2 bg-violet-400 text-white rounded-full block">
      {name}
    </span>
  {/each}
</div>
