# Open Graph och Twitter Cards för SiteVision

Piffa upp dina delningar i sociala medier med stöd för [Open Graph-protokollet][og] och [Twitter Cards][tc] i SiteVision.

![][beforeafter]

## Installation

Kopiera innehållet i filen [open-graph.vm][template] och klistra in det som ett [kodtillägg][codesnippet] i SiteVision. Förslagsvis på huset, så ärvs det nedåt till alla sidor på webbplatsen. Se till att kryssa i rutan *Kör som velocity*.

## Inställningar

Inställningarna ligger högst upp i mallen och det finns följande inställningar. Den läser ut metadata i den ordning som är specifierad i respektive _order_-inställningar, så fort den får ett värde så skriver den ut det.

### Titel

**titleOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:title_.

**renderTitleMeta:** Sätt till _false_ om inte meta-taggen ska renderas.

### Ingress

**preambleOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:description_.

**renderPreambleMeta:** Sätt till _false_ om inte meta-taggen ska renderas.

**renderPreambleAsDescription:** Om denna är _true_ skrivs även en <meta name="description"> ut om ett värde hittas. Om _renderPreambleMeta_ är false så skrivs inte denna ut även om den är _true_.

### Bilder

**imageOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:image_.

**renderImageMeta:** Sätt till false om inte meta-taggen ska renderas.

**imageFallbackUrl:** Den bild som ska användas om ingen bild hittas, om denna är relativ (och börjar med /) så kommer sajtens host läsas ut och läggas till innan.

**imageFallbackWidth** och **imageFallbackHeight:** Bredd och höjd på reserv-bilden.

## MIT-licens

Detta projekt är licensierat under MIT-licensen, se filen [LICENSE][license].

[og]: http://ogp.me
[tc]: https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards
[template]: open-graph.vm
[codesnippet]: https://help.sitevision.se/SiteVision_4_0/codeSnippetHelp.html
[license]: LICENSE
[beforeafter]: docs/before-and-after.png
