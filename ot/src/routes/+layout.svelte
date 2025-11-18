<script>
  import "../app.css";
  import favicon from "$lib/assets/favicon.svg";

  let { children } = $props();
</script>

<svelte:head>
  <title>oldtimer</title>
  <meta charset="utf-8" />
  <meta name="description" content="oldtimer and parts sourcing" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="theme-color" content="#000000" />

  <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "AutomotiveBusiness",
      "@id": "https://oldtimer.de/#business",
      "name": "Andrey Paymishin",
      "url": "https://oldtimer.de/paymushin",
      "telephone": "+49 170 1234567",
      "email": "andrey.paymishin@oldtimer.de",
      "image": "https://oldtimer.de/preview.png",
      "priceRange": "€€€",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "Musterstraße 1",
        "addressLocality": "Berlin",
        "addressRegion": "Berlin",
        "postalCode": "10115",
        "addressCountry": "DE"
      },
      "openingHours": "Mo,Tu,We,Th,Fr 10:00-18:00",
      "founder": {
        "@type": "Person",
        "name": "Andrey Paymishin"
      },
      "availableLanguage": [
        { "@type": "Language", "name": "German" },
        { "@type": "Language", "name": "English" }
      ]
    }
  </script>

  <link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
