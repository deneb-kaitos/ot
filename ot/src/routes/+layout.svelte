<script>
  import { dev } from "$app/environment";
  import "../app.css";
  import favicon from "$lib/assets/favicon.svg";

  let { data, children } = $props();
  const { siteInfo, JSONLD } = data;
</script>

<svelte:head>
  <title>{siteInfo.meta.description}</title>
  <meta charset="utf-8" />
  <meta name="description" content={siteInfo.meta.description} />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#000000" />
  {@html `<script type="application/ld+json">${JSON.stringify(JSONLD)}</script>`}
  <link rel="icon" href={favicon} />

  {#if !dev}
    <style>
      :root {
        pointer-events: none;
        user-select: none;
      }
    </style>
  {/if}
</svelte:head>

{@render children()}
