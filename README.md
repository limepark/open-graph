# Open Graph meta-taggar
Man lägger till denna i "Tillägg i HEAD" som _avancerad_ och _velocity_.

## Inställningar
Inställningarna ligger högst upp i mallen och det finns följande inställningar. Den läser ut metadata eller portlets i den ordning som är specifierad i respektive _order_-inställningar, så fort den får ett värde så skriver den ut det.

### Bilder
**imageOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:image_. Där det står _Portlet_ så kommer den istället hämta ut en bildportlet med namnet som är konfigurerat.

**imagePortletName:** Namnet på den bildportlet som ska läsas upp vid typen _Portlet_.

**imageFallbackUrl:** Den bild som ska användas om ingen bild hittas, om denna är relativ (och börjar med /) så kommer sajtens host läsas ut och läggas till innan.

**renderImageMeta:** Sätt till false om inte meta-taggen ska renderas.

### Ingress
**preambleOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:description_. Där det står _Portlet_ så kommer den istället hämta ut en textportlet med namnet som är konfigurerat.

**preamblePortletName:** Namnet på den text som ska läsas upp vid typen _Portlet_.

**renderPreambleMeta:** Sätt till _false_ om inte meta-taggen ska renderas.

**renderPreambleAsDescription:** Om denna är _true_ skrivs även en <meta name="description"> ut om ett värde hittas. Om _renderPreambleMeta_ är false så skrivs inte denna ut även om den är _true_.

### Titel
**titleOrder:** Den ordning som den ska försöka hämta metadatavärden som ska skrivas ut som _og:title_. Där det står _Portlet_ så kommer den istället hämta ut en textportlet med namnet som är konfigurerat.

**titlePortletName:** Namnet på den text som ska läsas upp vid typen _Portlet_.

**renderTitleMeta:** Sätt till _false_ om inte meta-taggen ska renderas.