# 🤯 HEAD

> Un guia simple sobre como usar el elemento `<head>` en HTML

[![Contributors](https://img.shields.io/github/contributors/joshbuchea/head.svg?style=for-the-badge)](https://github.com/joshbuchea/HEAD/graphs/contributors)
[![CC0](https://img.shields.io/badge/license-CC0-green.svg?style=for-the-badge)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Follow @joshbuchea on Mastodon](https://img.shields.io/badge/Follow_@joshbuchea-purple?logo=mastodon&logoColor=white&style=for-the-badge)](https://hachyderm.io/@joshbuchea)

## Tabla de Contenidos

- [Mínimos recomendados](#mínimos-recomendados)
- [Elementos](#elementos)
- [Meta](#meta)
- [Enlaces](#enlaces)
- [Iconos](#iconos)
- [Social](#social)
  - [Facebook Open Graph](#facebook-open-graph)
  - [Twitter Card](#twitter-card)
  - [Twitter Privacy](#twitter-privacy)
  - [Schema.org](#schemaorg)
  - [Pinterest](#pinterest)
  - [Facebook Instant Articles](#facebook-instant-articles)
  - [OEmbed](#oembed)
  - [QQ/Wechat](#qqwechat)
- [Navegadores / Plataformas](#navegadores--plataformas)
  - [Apple iOS](#apple-ios)
  - [Google Android](#google-android)
  - [Google Chrome](#google-chrome)
  - [Microsoft Internet Explorer](#microsoft-internet-explorer)
- [Navegadores (Chinos)](#navegadores-chinos)
  - [360 Browser](#360-browser)
  - [QQ Mobile Browser](#qq-mobile-browser)
  - [UC Mobile Browser](#uc-mobile-browser)
- [Enlaces de aplicaciones](#enlaces-de-aplicaciones)
- [Otros recursos](#otros-recursos)
- [Proyectos relacionados](#proyectos-relacionados)
- [Otros formatos](#otros-formatos)
- [Traducciones](#-traducciones)
- [Colaboradores](#-colaboradores)
- [Autor de la traducción](#-autor-de-la-traducción)
- [Autor](#-autor)
- [Soporte al proyecto original](#💛-soporte-al-proyecto-original)
- [Licencia](#-licencia)

## Mínimos recomendados

A continuación se muestran los elementos esenciales para cualquier documento web (sitios web/aplicaciones):

```html
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<!--
  Las 2 metaetiquetas anteriores *deben* aparecer primero en el <head> para asegurar consistentemente la representación adecuada del documento.
  Cualquier otro elemento principal debe ir *después* de estas etiquetas.
 -->
<title>Título de la página</title>
```

`meta charset` - define la codificación del sitio web, `utf-8` es el estándar

`meta name="viewport"` - configuración de la vista relacionada con la capacidad de respuesta móvil

`width=device-width` - usa el ancho físico del dispositivo (¡excelente para dispositivos móviles!)

`initial-scale=1` - el zoom inicial, 1 significa que no hay zoom

**[⬆ volver arriba](#tabla-de-contenidos)**

## Elementos

Los elementos `<head>` válidos incluyen `meta`, `link`, `title`, `style`, `script`, `noscript` y `base`.

Estos elementos proporcionan información sobre cómo las tecnologías web deben percibir y representar un documento. p.ej. navegadores, motores de búsqueda, bots, etc.

```html
<!--
  Configure la codificación de caracteres para este documento, de modo que todos los caracteres dentro del espacio UTF-8 (como emoji) se representan correctamente.
-->
<meta charset="utf-8">

<!-- Establece el título del documento. -->
<title>Page Title</title>

<!-- Establece la URL base para todas las URL relativas dentro del documento. -->
<base href="https://ejemplo.com/pagina.html">

<!-- Enlace a un archivo CSS externo -->
<link rel="stylesheet" href="estilos.css">

<!-- Se utiliza para agregar CSS en el documento -->
<style>
  /* ... */
</style>

<!-- Etiquetas de JavaScript y sin JavaScript -->
<script src="script.js"></script>
<script>
  // la(s) función(es) van aquí
</script>
<noscript>
  <!-- No hay alternativa JS -->
</noscript>
```

**[⬆ volver arriba](#tabla-de-contenidos)**

## Meta

```html
<!--
  Las 2 metaetiquetas anteriores *deben* aparecer primero en el <head> para asegurar consistentemente la representación adecuada del documento.
  Cualquier otro elemento principal debe ir *después* de estas etiquetas.
-->
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<!--
  Permite controlar desde dónde se cargan los recursos.
  Coloque lo más temprano posible en <head>, como la etiqueta solo se aplica a los recursos que se declaran después.
-->
<meta http-equiv="Content-Security-Policy" content="default-src 'self'">

<!-- Nombre de la aplicación web (solo debe usarse si el sitio web se usa como una aplicación) -->
<meta name="application-name" content="Nombre de la aplicación">

<!-- Color del tema para Chrome, Firefox OS y Opera -->
<meta name="theme-color" content="#4285f4">

<!-- Breve descripción del documento (límite de 150 caracteres) -->
<!-- Este contenido *puede* ser utilizado como parte de los resultados del motor de búsqueda. -->
<meta name="description" content="Una descripción de la página">

<!-- Controla el comportamiento del rastreo y la indexación de los motores de búsqueda -->
<meta name="robots" content="index,follow"><!-- Todos los motores de búsqueda -->
<meta name="googlebot" content="index,follow"><!-- Específico de Google -->

<!-- Le dice a Google que no muestre el cuadro de búsqueda de enlaces de sitio -->
<meta name="google" content="nositelinkssearchbox">

<!-- Le dice a Google que no proporcione una traducción para este documento -->
<meta name="google" content="notranslate">

<!-- Verificar la propiedad del sitio web -->
<meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
<meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
<meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
<meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
<meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
<meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->

<!-- Identifica el software utilizado para crear el documento (es decir, WordPress, Dreamweaver) -->
<meta name="generator" content="program">

<!-- Breve descripción del tema de su documento -->
<meta name="subject" content="el tema de su documento">

<!-- Da una clasificación de edad general basada en el contenido del documento. -->
<meta name="rating" content="General">

<!-- Permite controlar cómo se pasa la información de referencia. -->
<meta name="referrer" content="no-referrer">

<!-- Deshabilita la detección automática y el formateo de posibles números de teléfono -->
<meta name="format-detection" content="telephone=no">

<!-- Opte completamente por la obtención previa de DNS configurando en "desactivado" -->
<meta http-equiv="x-dns-prefetch-control" content="off">

<!-- Especifica el documento para que aparezca en un marco específico -->
<meta http-equiv="Window-Target" content="_value">

<!-- Etiquetas geográficas -->
<meta name="ICBM" content="latitud, longitud">
<meta name="geo.position" content="latitud;longitud">
<meta name="geo.region" content="pais[-provincia]"><!-- Código de país (ISO 3166-1): obligatorio, código de estado (ISO 3166-2): opcional; p.ej. contenido = "ES" / contenido = "ES.-MAD" -->
<meta name="geo.placename" content="ciudad/pueblo"><!-- p.ej. content="Madrid" -->

<!-- Web Monetization https://webmonetization.org/docs/getting-started -->
<meta name="monetization" content="$paymentpointer.example">
```

- 📖 [Metaetiquetas que Google entiende](https://support.google.com/webmasters/answer/79812?hl=en)
- 📖 [Wiki de WHATWG: MetaExtensions](https://wiki.whatwg.org/wiki/MetaExtensions)
- 📖 [ICBM en la Wikipedia](https://en.wikipedia.org/wiki/ICBM_address#Modern_use)
- 📖 [Geoetiquetado en Wikipedia](https://en.wikipedia.org/wiki/Geotagging#HTML_pages)

**[⬆ volver arriba](#tabla-de-contenido)**

## Enlaces

```html
<!-- Apunta a una hoja de estilo externa -->
<link rel="stylesheet" href="https://ejemplo.com/estilos.css">

<!-- Ayuda a prevenir problemas de contenido duplicado -->
<link rel="canonical" href="https://ejemplo.com/articulo/?pagina=2">

<!-- Enlaces a una versión AMP HTML del documento actual -->
<link rel="amphtml" href="https://ejemplo.com/ruta/a/la/version-amp.html">

<!-- Enlaces a un archivo JSON que especifica las credenciales de "instalación" para las aplicaciones web -->
<link rel="manifest" href="manifest.json">

<!-- Enlaces a información sobre el(los) autor(es) del documento -->
<link rel="author" href="humanos.txt">

<!-- Se refiere a una declaración de derechos de autor que se aplica al contexto del enlace. -->
<link rel="license" href="copyright.html">

<!-- Da una referencia a una ubicación en su documento que puede estar en otro idioma -->
<link rel="alternate" href="https://en.ejemplo.com/" hreflang="en">

<!-- Proporciona información sobre un autor u otra persona. -->
<link rel="me" href="https://google.com/profiles/thenextweb" type="text/html">
<link rel="me" href="mailto:nombre@ejemplo.com">
<link rel="me" href="sms:+34000000000">

<!-- Enlaces a un documento que describe una colección de registros, documentos u otros materiales de interés histórico -->
<link rel="archives" href="https://ejemoplo.com/archivos/">

<!-- Enlaces a recursos de nivel superior en una estructura jerárquica -->
<link rel="index" href="https://ejemplo.com/articulo/">

<!-- Proporciona una referencia propia: útil cuando el documento tiene varias referencias posibles. -->
<link rel="self" type="application/atom+xml" href="https://ejemplo.com/atom.xml">

<!-- Los documentos primero, último, anterior y siguiente de una serie de documentos, respectivamente -->
<link rel="first" href="https://ejemplo.com/articulo/">
<link rel="last" href="https://ejemplo.com/articulo/?pagina=42">
<link rel="prev" href="https://ejemplo.com/articulo/?pagina=1">
<link rel="next" href="https://ejemplo.com/articulo/?pagina=3">

<!-- Se utiliza cuando se utiliza un servicio de terceros para mantener un blog. -->
<link rel="EditURI" href="https://ejemplo.com/xmlrpc.php?rsd" type="application/rsd+xml" title="RSD">

<!-- Forma un comentario automático cuando otro blog de WordPress se vincula a su blog o publicación de WordPress -->
<link rel="pingback" href="https://ejemplo.com/xmlrpc.php">

<!-- Notifica una URL cuando se vincula a ella en su documento -->
<link rel="webmention" href="https://ejemplo.com/webmention">

<!-- Habilita la publicación en su propio dominio usando un cliente Micropub -->
<link rel="micropub" href="https://ejemplo.com/micropub">

<!-- Open Search -->
<link rel="search" href="/open-search.xml" type="application/opensearchdescription+xml" title="Título de búsqueda">

<!-- Feeds -->
<link rel="alternate" href="https://feeds.feedburner.com/example" type="application/rss+xml" title="RSS">
<link rel="alternate" href="https://ejemplo.com/feed.atom" type="application/atom+xml" title="Atom 0.3">

<!-- Precarga, precarga, prenavegación -->
<!-- Más información: https://css-tricks.com/prefetching-preloading-prebrowsing/ -->
<link rel="dns-prefetch" href="//ejemplo.com/">
<link rel="preconnect" href="https://www.ejemplo.com/">
<link rel="prefetch" href="https://www.ejemplo.com/">
<link rel="prerender" href="https://ejemplo.com/">
<link rel="preload" href="imagen.png" as="image">
```

- 📖 [Enlaces relacionados](https://www.iana.org/assignments/link-relations/link-relations.xhtml)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Iconos

```html
<!-- Para IE 10 y menos -->
<!-- Coloque favicon.ico en el directorio raíz; no se necesita etiqueta -->

<!-- Icono en la máxima resolución para lo que lo necesitamos -->
<link rel="icon" sizes="192x192" href="/ruta/al/icono.png">

<!-- Ícono Apple Touch (reutilizar 192px icono.png) -->
<link rel="apple-touch-icon" href="/ruta/al/icono-apple-touch.png">

<!-- Icono de pestaña anclada de Safari -->
<link rel="mask-icon" href="/ruta/al/icono.svg" color="blue">
```

- 📖 [Todo sobre Favicons (e íconos táctiles)](https://bitsofco.de/all-about-favicons-and-touch-icons/)
- 📖 [Creación de iconos de pestañas ancladas](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/pinnedTabs/pinnedTabs.html)
- 📖 [Hoja de referencia de Favicon](https://github.com/audreyr/favicon-cheat-sheet)
- 📖 [Iconos y colores del navegador](https://developers.google.com/web/fundamentals/design-and-ux/browser-customization/)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Social

### Facebook Open Graph
> La mayoría del contenido se comparte en Facebook como una URL, por lo que es importante que marque su sitio web con etiquetas Open Graph para controlar cómo aparece su contenido en Facebook.. [Más acerca del Facebook Open Graph Markup](https://developers.facebook.com/docs/sharing/webmasters#markup) 

```html
<meta property="fb:app_id" content="123456789">
<meta property="og:url" content="https://ejemplo.com/page.html">
<meta property="og:type" content="website">
<meta property="og:title" content="Título del contenido">
<meta property="og:image" content="https://ejemplo.com/imagen.jpg">
<meta property="og:image:alt" content="Una descripción de lo que está en la imagen (no un pie de foto)">
<meta property="og:description" content="Descripción Aquí">
<meta property="og:site_name" content="Nombre del sitio">
<meta property="og:locale" content="es">
<meta property="article:author" content="">
```

- 📖 [Protocolo Open Graph](http://ogp.me/)
- 🛠 Pon a prueba tu página con el [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)

### Twitter Card
> Con Twitter Cards, puede adjuntar fotos, videos y experiencias multimedia enriquecidas a los Tweets, lo que ayuda a atraer tráfico a su sitio web. [Más acerca de Twitter Cards](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

```html
<meta name="twitter:card" content="summary">
<meta name="twitter:site" content="@cuenta_del_sitio">
<meta name="twitter:creator" content="@cuenta_individual">
<meta name="twitter:url" content="https://ejemplo.com/pagina.html">
<meta name="twitter:title" content="Título del contenido">
<meta name="twitter:description" content="Descripción del contenido de menos de 200 caracteres">
<meta name="twitter:image" content="https://ejemplo.com/imagen.jpg">
<meta name="twitter:image:alt" content="Una descripción de texto de la imagen que transmite la naturaleza esencial de una imagen a los usuarios con discapacidad visual. Máximo 420 caracteres.">
```

- 📖 [Empezando con tarjetas — Twitter Developers](https://dev.twitter.com/cards/getting-started)
- 🛠 Pon a prueba tu página con el [Twitter Card Validator](https://cards-dev.twitter.com/validator)

### Twitter Privacy
Si inserta tweets en su sitio web, Twitter puede usar la información de su sitio para adaptar el contenido y las sugerencias a los usuarios de Twitter. [Más sobre las opciones de Twitter privacy](https://dev.twitter.com/web/overview/privacy#what-privacy-options-do-website-publishers-have).
```html
<!-- prohibir que Twitter use la información de su sitio para fines de personalización -->
<meta name="twitter:dnt" content="on">
```

### Schema.org

```html
<html lang="" itemscope itemtype="https://schema.org/Article">
    <head>
      <link rel="author" href="">
      <link rel="publisher" href="">
      <meta itemprop="name" content="Título del contenido">
      <meta itemprop="description" content="Descripción del contenido de menos de 200 caracteres">
      <meta itemprop="image" content="https://ejemplo.com/imagen.jpg">
```

**Nota:** Estas etiquetas meta requieren que se agreguen los atributos `itemscope` y `itemtype` a la etiqueta `<html>`.

- 📖 [Empezando con - schema.org](https://schema.org/docs/gs.html)
- 🛠 Pon a prueba tu página con el [Rich Results Test](https://search.google.com/test/rich-results)

### Pinterest

Pinterest te permite evitar que la gente guarde cosas de tu sitio web, según su [centro de ayuda](https://help.pinterest.com/en/business/article/prevent-saves-to-pinterest-from-your-site). La `descripción` es opcional.

```html
<meta name="pinterest" content="nopin" description="¡Lo siento, no puedes guardar desde mi sitio web!">
```

### Facebook Instant Articles

```html
<meta charset="utf-8">
<meta property="op:markup_version" content="v1.0">

<!-- The URL of the web version of your article -->
<link rel="canonical" href="https://ejemplo.com/articulo.html">

<!-- The style to be used for this article -->
<meta property="fb:article_style" content="myarticlestyle">
```

- 📖 [Creando articulos - Instant Articles](https://developers.facebook.com/docs/instant-articles/guides/articlecreate)
- 📖 [Ejemplos de código - Instant Articles](https://developers.facebook.com/docs/instant-articles/reference)

### OEmbed

```html
<link rel="alternate" type="application/json+oembed"
  href="https://ejemplo.com/servicios/oembed?url=http%3A%2F%2Fejemplo.com%2Ffoo%2F&amp;format=json"
  title="oEmbed Profile: JSON">
<link rel="alternate" type="text/xml+oembed"
  href="https://ejemplo.com/servicios/oembed?url=http%3A%2F%2Fejemplo.com%2Ffoo%2F&amp;format=xml"
  title="oEmbed Profile: XML">
```

- 📖 [Formato oEmbed](https://oembed.com/)

### QQ/Wechat

Los usuarios comparten páginas web para q wechat tenga un mensaje formateado

```html
<meta itemprop="name" content="share title">
<meta itemprop="image" content="http://imgcache.qq.com/qqshow/ac/v4/global/logo.png">
<meta name="description" itemprop="description" content="share content">
```
- 📖 [Documentos de formato de código](http://open.mobile.qq.com/api/mqq/index#api:setShareInfo)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Navegadores / Plataformas

### Apple iOS

```html
<!-- Smart App Banner -->
<meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">

<!-- Deshabilite la detección automática y el formateo de posibles números de teléfono -->
<meta name="format-detection" content="telephone=no">

<!-- Launch Icon (180x180px o más grande) -->
<link rel="apple-touch-icon" href="/ruta/al/icono-apple-touch.png">

<!-- Launch Screen Image -->
<link rel="apple-touch-startup-image" href="/ruta/a/launch.png">

<!-- Launch Icon Title -->
<meta name="apple-mobile-web-app-title" content="Título de la aplicación">

<!-- Habilitar el modo independiente (pantalla completa) -->
<meta name="apple-mobile-web-app-capable" content="yes">

<!-- Apariencia de la barra de estado (no tiene efecto a menos que el modo independiente esté habilitado) -->
<meta name="apple-mobile-web-app-status-bar-style" content="black">

<!-- iOS app deep linking -->
<meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-de-ejemplo.com">
<link rel="alternate" href="ios-app://APP-ID/http/url-de-ejemplo.com">
```

- 📖 [Configuración de aplicaciones web](https://developer.apple.com/library/content/documentation/AppleApplications/Reference/SafariWebContent/ConfiguringWebApplications/ConfiguringWebApplications.html)

### Google Android

```html
<meta name="theme-color" content="#E64545">

<!-- Añadir a pantalla de inicio -->
<meta name="mobile-web-app-capable" content="yes">
<!-- Más información: https://developer.chrome.com/multidevice/android/installtohomescreen -->

<!-- Android app deep linking -->
<meta name="google-play-app" content="app-id=package-name">
<link rel="alternate" href="android-app://package-name/http/url-de-ejemplo.com">
```

### Google Chrome

```html
<link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">

<!-- Deshabilitar solicitud de traducción -->
<meta name="google" content="notranslate">
```

### Microsoft Internet Explorer

```html
<!-- Forzar a IE 8/9/10 a usar su último motor de renderizado -->
<meta http-equiv="x-ua-compatible" content="ie=edge">

<!-- Deshabilite la detección automática y el formateo de posibles números de teléfono mediante la extensión del navegador de la barra de herramientas de Skype -->
<meta name="skype_toolbar" content="skype_toolbar_parser_compatible">

<!-- Windows Tiles -->
<meta name="msapplication-config" content="/browserconfig.xml">
```

Marcado xml mínimo requerido para `browserconfig.xml`:

```xml
<?xml version="1.0" encoding="utf-8"?>
<browserconfig>
   <msapplication>
     <tile>
        <square70x70logo src="pequeño.png"/>
        <square150x150logo src="mediano.png"/>
        <wide310x150logo src="ancho.png"/>
        <square310x310logo src="largo.png"/>
     </tile>
   </msapplication>
</browserconfig>
```

- 📖 [Referencia del esquema de configuración del navegador](https://msdn.microsoft.com/en-us/library/dn320426.aspx)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Navegadores (Chinos)

### 360 Browser

```html
<!-- Seleccione el orden del motor de renderizado -->
<meta name="renderer" content="webkit|ie-comp|ie-stand">
```

### QQ Mobile Browser

```html
<!-- Bloquea la pantalla en la orientación especificada -->
<meta name="x5-orientation" content="landscape/portrait">

<!-- Mostrar este documento en pantalla completa -->
<meta name="x5-fullscreen" content="true">

<!-- El documento se mostrará en "modo de aplicación" (pantalla completa, etc.) -->
<meta name="x5-page-mode" content="app">
```

### UC Mobile Browser

```html
<!-- Bloquea la pantalla en la orientación especificada -->
<meta name="screen-orientation" content="landscape/portrait">

<!-- Mostrar este documento en pantalla completa -->
<meta name="full-screen" content="yes">

<!-- El navegador UC mostrará imágenes incluso si está en "modo de texto" -->
<meta name="imagemode" content="force">

<!-- El documento se mostrará en "modo de aplicación" (pantalla completa, gesto de prohibición, etc.) -->
<meta name="browsermode" content="application">

<!-- Se deshabilitó el "modo nocturno" del navegador UC para este documento -->
<meta name="nightmode" content="disable">

<!-- Simplificar el documento para reducir la transferencia de datos -->
<meta name="layoutmode" content="fitscreen">

<!-- Deshabilite la característica del navegador UC de "escalar la fuente cuando hay muchas palabras en este documento" -->
<meta name="wap-font-scale" content="no">
```

- 📖 [Documentación de UC Browser](https://www.uc.cn/download/UCBrowser_U3_API.doc)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Enlaces de aplicaciones

```html
<!-- iOS -->
<meta property="al:ios:url" content="applinks://docs">
<meta property="al:ios:app_store_id" content="12345">
<meta property="al:ios:app_name" content="Enlaces de aplicaciones">

<!-- Android -->
<meta property="al:android:url" content="applinks://docs">
<meta property="al:android:app_name" content="Enlaces de aplicaciones">
<meta property="al:android:package" content="org.applinks">

<!-- Web fall back -->
<meta property="al:web:url" content="https://applinks.org/documentation">
```

- 📖 [Enlaces de aplicaciones](https://developers.facebook.com/docs/applinks)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Otros recursos

- 📖 [HTML5 Boilerplate Docs: The HTML](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/html.md)
- 📖 [HTML5 Boilerplate Docs: Extend and customize](https://github.com/h5bp/html5-boilerplate/blob/master/dist/doc/extend.md)

**[⬆ volver arriba](#tabla-de-contenidos)**

## Proyectos relacionados

- [Atom HTML Head Snippets](https://github.com/joshbuchea/atom-html-head-snippets) - Atom package for `HEAD` snippets
- [Sublime Text HTML Head Snippets](https://github.com/marcobiedermann/sublime-head-snippets) - Sublime Text package for `HEAD` snippets
- [head-it](https://github.com/hemanth/head-it) - CLI interface for `HEAD` snippets
- [vue-head](https://github.com/ktquez/vue-head) - Manipulating the meta information of the `HEAD` tag for Vue.js

**[⬆ volver arriba](#tabla-de-contenidos)**

## Otros formatos

- 📄 [PDF](https://gitprint.com/joshbuchea/HEAD/blob/master/README.md)

**[⬆ volver arriba](#tabla-de-contenidos)**

## 🌐 Traducciones

- 🇮🇩 [Bahasa](https://github.com/rijdz/HEAD)
- 🇧🇷 [Brazilian Portuguese](https://github.com/Webschool-io/HEAD)
- 🇨🇳 [Chinese (Simplified)](https://github.com/Amery2010/HEAD)
- 🇩🇪 [German](https://github.com/Shidigital/HEAD)
- 🇮🇹 [Italian](https://github.com/Fakkio/HEAD)
- 🇯🇵 [Japanese](https://coliss.com/articles/build-websites/operation/work/collection-of-html-head-elements.html)
- 🇰🇷 [Korean](https://github.com/Lutece/HEAD)
- 🇷🇺 [Russian/Русский](https://github.com/Konfuze/HEAD)
- 🇺🇸 [English](https://github.com/joshbuchea/HEAD)
- 🇹🇷 [Turkish/Türkçe](https://github.com/mkg0/HEAD)

**[⬆ volver arriba](#tabla-de-contenidos)**

## 🌟 Colaboradores

Echa un vistazo a todos los super impresionantes [colaboradores/as](https://github.com/joshbuchea/HEAD/graphs/contributors) 🤩

## 👤 Autor de la traducción

**Álvaro Araoz**

- GitHub: [@alvaroadlf](https://github.com/alvaroadlf)
- Web: [imalvaro.com](https://imalvaro.com)
- Twitter: [@alvaroaraoz](https://twitter.com/alvaroaraoz)

## 👤 Autor

**Josh Buchea**

- GitHub: [@joshbuchea](https://github.com/joshbuchea)
- Mastodon: [@joshbuchea@hachyderm.io](https://hachyderm.io/@joshbuchea)

## 💛 Soporte al proyecto original

Si este proyecto fue útil para usted o su organización, considere apoyar mi trabajo directamente:

- 💛 [Patrocíname en GitHub](https://github.com/sponsors/joshbuchea)
- ⭐️ [Destaca este proyecto en GitHub](https://github.com/joshbuchea/HEAD)
- 🐙 [sígueme en GitHub](https://github.com/joshbuchea)
- 🐘 [Sígueme en Mastodon](https://hachyderm.io/@joshbuchea)

¡Todo ayuda, gracias! 🙏

— Josh

## 📝 Licencia

[![CC0](https://i.creativecommons.org/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

**[⬆ volver arriba](#tabla-de-contenidos)**
