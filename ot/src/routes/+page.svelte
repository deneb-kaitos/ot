<article>
  <header>oldtimer sourcing</header>
  <div class="name-position-service">
    <h1 class="name">Andrey Paymushin</h1>
    <h2 class="position">founder / CEO</h2>
    <h3 class="service">oldtimeer & parts sourcing</h3>
  </div>
  <dl class="contacts">
    <dt>T</dt>
    <dd>+49 000 12345678</dd>

    <dt>E</dt>
    <dd>andrey.paymushin@oldtimer.de</dd>
  </dl>
  <footer>based in Germany</footer>
</article>

<style>
  :root {
    /* global color scheme */
    --root-background-color: hsl(240deg 6.67% 97.06%);
    --root-color: hsl(0deg 0% 10.2%);
    --article-background-color: hsl(0deg 0% 100%);
    --filter-drop-shadow-color: hsl(0deg 0% 81.72%);

    /* global defaults */
    --article-padding: 2.5vw;
    --article-padding-top: 0.5vw;
    --article-padding-bottom: var(--article-padding-top);
    --article-border-radius: 2px;
    --article-min-width: 40vw;
    --article-aspect-ratio: 5 / 3;
    --article-column-gap: 0.5vw;
    --article-row-gap: 1vh;
    --article-filter: drop-shadow(2px 4px 6px var(--filter-drop-shadow-color));
    --header-footer-margin-size: 2.5vh;

    /* global defaults applied */
    color: var(--root-color);
    background-color: var(--root-background-color);
  }

  article {
    container: article / inline-size;
    display: grid;
    grid-template-columns: var(--article-padding) 1fr var(--article-padding);
    grid-template-rows: var(--article-padding-top) auto 3fr 1fr auto var(
        --article-padding-bottom
      );
    grid-template-areas:
      ". . ."
      ". header ."
      ". name-position-service ."
      ". contacts ."
      ". footer ."
      ". . .";
    column-gap: var(--article-column-gap);
    row-gap: var(--article-row-gap);

    align-self: center;
    justify-self: center;
    aspect-ratio: var(--article-aspect-ratio);
    min-width: var(--article-min-width);
    border-radius: var(--article-border-radius);
    color: var(--color);

    background-color: var(--article-background-color);
    filter: var(--article-filter);

    & > :is(header, footer) {
      display: flex;
      justify-content: center;
      align-items: center;
      text-transform: uppercase;
      font-variant: all-petite-caps;
      font-size: small;
      color: var(--filter-drop-shadow-color);
    }

    & > header {
      grid-area: header;
      margin-bottom: var(--header-footer-margin-size);
    }

    & > .name-position-service {
      container: name-position-service / inline-size;
      grid-area: name-position-service;
      display: grid;
      grid-template-columns: var(--article-padding) 1fr var(--article-padding);
      grid-template-rows: 2fr 1fr 2fr;
      grid-template-areas:
        ". name ."
        ". position ."
        ". service .";
      column-gap: var(--article-column-gap);
      row-gap: calc(var(--article-row-gap) * 0.75);

      & > :is(.name, .position, .service) {
        display: flex;
        justify-content: center;
        margin: 0;
      }

      & > .name {
        grid-area: name;
        display: flex;
        align-items: end;
        margin-bottom: calc(var(--header-footer-margin-size) * 0.35);
      }

      & > .position {
        grid-area: position;
        align-items: center;
      }

      & > .service {
        grid-area: service;
        align-items: start;
        margin-top: calc(var(--header-footer-margin-size) * 0.35);
      }
    }

    & > .contacts {
      container: contacts / inline-size;
      grid-area: contacts;
      display: grid;
      grid-template-columns: auto 1fr;
      justify-content: stretch;
      align-items: center;
      margin: 0;
      width: 50%;
      justify-self: center;

      & > :is(dt, dd) {
        display: flex;
        align-items: center;
      }

      & > dt {
        grid-column: 1;
        aspect-ratio: 1 / 1;
        height: 100%;
        justify-content: center;
        color: var(--filter-drop-shadow-color);
      }

      & > dd {
        grid-column: 2;
        margin-inline-start: unset;
        border-bottom: 1px dotted var(--filter-drop-shadow-color);
        justify-content: end;
      }
    }

    & > footer {
      grid-area: footer;
      margin-top: var(--header-footer-margin-size);
    }
  }
</style>
