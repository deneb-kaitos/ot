<script>
  import "../app.css";
  import favicon from "$lib/assets/favicon.svg";

  let { children } = $props();
</script>

<svelte:head>
  <script type="application/ld+json">
    {
      "@context": "https://schema.org",
      "@type": "AutomotiveBusiness",
      "@id": "https://oldtimer.de/#business",
      "name": "Andrey Paymishin",
      "url": "https://oldtimer.com/paymushin",
      "telephone": "+49 170 1234567",
      "areaServed": {
        "@type": "Country",
        "name": "Germany"
      },
      "founder": {
        "@type": "Person",
        "name": "Andrey Paymishin"
      },
      "currenciesAccepted": "EUR",
      "openingHours": "Mo,Tu,We,Th,Fr 10:00-18:00",
      "paymentAccepted": "Cash, Credit Card",
      "priceRange": "$$$",
      "address": {
        "@type": "PostalAddress",
        "addressCountry": "DE",
        "addressLocality": "Berlin",
        "addressRegion": "Berlin"
      },
      "availableLanguage": [
        {
          "@type": "Language",
          "name": "German"
        },
        {
          "@type": "Language",
          "name": "English"
        }
      ],
      "email": "andrey.paymishin@oldtimer.de",
      "keywords": "oldtimer sourcing, classic car sourcing, classic car finder, oldtimer parts finder, rare automotive parts, off-market classic cars, collector car sourcing, europe classic cars"
    }
  </script>

  <link rel="icon" href={favicon} />
</svelte:head>

{@render children()}
