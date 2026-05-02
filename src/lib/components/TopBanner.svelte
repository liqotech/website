<script>
  let { children=null, link="" } = $props();
</script>

{#if children}
    <div class="bg-accent text-accent-content text-center text-md font-medium py-2">
        {#if link}
            <a href="{link}" class="link link-hover" target="_blank">
                {@render children()}
            </a>
        {:else}
            {@render children()}
        {/if}
    </div>
{/if}