# Open Graph-protokollet och Twitter Cards

Stöd för [Open Graph-protokollet][1] och [Twitter Cards][2] i SiteVision.

Du lägger `open-graph.vm` som ett [kodtillägg][3]. Förslagsvis på huset, så det ärvs nedåt.

## Inställningar

Inställningarna ligger högst upp i mallen och det finns följande inställningar. Den läser ut metadata i den ordning som är specifierad i respektive _order_-inställningar, så fort den får ett värde så skriver den ut det.

### Bilder

**imageOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:image_.

**imageFallbackUrl:** Den bild som ska användas om ingen bild hittas, om denna är relativ (och börjar med /) så kommer sajtens host läsas ut och läggas till innan.

**imageFallbackWidth** och *imageFallbackHeight:* Bredd och höjd på reserv-bilden.

**renderImageMeta:** Sätt till false om inte meta-taggen ska renderas.

### Ingress

**preambleOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:description_.

**renderPreambleMeta:** Sätt till _false_ om inte meta-taggen ska renderas.

**renderPreambleAsDescription:** Om denna är _true_ skrivs även en <meta name="description"> ut om ett värde hittas. Om _renderPreambleMeta_ är false så skrivs inte denna ut även om den är _true_.

### Titel

**titleOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:title_.

**renderTitleMeta:** Sätt till _false_ om inte meta-taggen ska renderas.

[1]: http://ogp.me
[2]: https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards
[3]: https://help.sitevision.se/SiteVision_4_0/codeSnippetHelp.html
