Good to mention these facts:

*   Dynamic title tag
*   Dynamic description meta tag
    *   Dynamic facebook description tag
    *   Dynamic twitter description tag
*   Not too long keyword tag (which mostly is ignored my Google these days)
*   Very high quality contents
*   Speed performance
    *   by minimizing your css
    *   by minimizing your javascript
*   robot.txt file
*   sitemap.xml file
*   Google webmaster tools
*   Using alt tags fro images
*   Using title tag for most HTML tags
*   Optimize images for better download
*   Avoid using flash
*   [have a look at here](https://support.google.com/webmasters/topic/6001981?hl=en&ref_topic=3309300)

Something like this:

```xml
<title>@yield('title', config('app.name'))</title>
<meta name="description" content="@yield('description', config('app.description'))"/>
<meta name="keywords" content="@yield('keywords', config('app.keywords'))"/>
<meta name="copyright" content="{{ config('app.name') }}">
<meta name="author" content="{{ config('app.name') }}"/>
<meta name="application-name" content="@yield('title', config('app.name'))">
<!--GEO Tags-->
<meta name="DC.title" content="@yield('title', config('app.name'))"/>
<meta name="geo.region" content="GB-HMF"/>
<meta name="geo.placename" content="London"/>
<meta name="geo.position" content="51.493272;-0.239747"/>
<meta name="ICBM" content="51.493272, -0.239747"/>
<!--Facebook Tags-->
<meta property="og:site_name" content="{{ config('app.name') }}">
<meta property="og:type" content="article"/>
<meta property="og:url" content="{{ request()->fullUrl() }}"/>
<meta property="og:title" content="@yield('title', config('app.name'))"/>
<meta property="og:description" content="@yield('description', config('app.description'))"/>
<meta property="og:image" content="{{ request()->root() }}/images/TODO.png"/>
<meta property="article:author" content="https://www.facebook.com/TODO"/>
<meta property="og:locale" content="en_UK"/>
<!--Twitter Tags-->
<meta name="twitter:card" content="summary"/>
<meta name="twitter:site" content="{{ '@' . config('app.name') }}"/>
<meta name="twitter:title" content="@yield('title', config('app.name'))"/>
<meta name="twitter:description" content="@yield('description', config('app.description'))"/>
<meta name="twitter:image" content="{{ request()->root() }}/images/TODO.png"/>
```

source: https://laracasts.com/discuss/channels/general-discussion/seo-and-laravel/replies/342116
