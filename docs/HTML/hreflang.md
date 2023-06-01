# `hreflang`について

`hreflang`はどの地域・言語をターゲットとしたページなのかを明確にするもの。検索エンジン側である程度自動で判断されるが、明示的に指定することでスコアをあげられることがある。

## 設定方法

### HTML

```html
<link rel="alternate" hreflang="en" href="https://example.com/en/">
```

### HTTP Header

```
Link: < https://example.com/file.pdf>; rel="alternate"; hreflang="jp",
　<https://example.com/zh/ file.pdf >; rel="alternate"; hreflang="zh",
　<https://example.com/en/ file.pdf >; rel="alternate"; hreflang="en"
```

### sitemap.xml

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9"
xmlns:xhtml="http://www.w3.org/1999/xhtml">
<url>
　<loc>https://example.com/</loc>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="jp"
　　　　href="https://example.com/"/>
　<xhtml:link
　　　 rel="alternate"
　　　　hreflang="en"
　　　 href="https://example.com/en/"/>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="zh-Hans"
　　　　href=" https://example.com/ch/"/>
</url>
<url>
　<loc> https://example.com/en/</loc>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="jp"
　　　　href="https://example.com/"/>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="en"
　　　　href="https://example.com/en/"/>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="zh-Hans"
　　　　href=" https://example.com/ch/"/>
</url>
<url>
　<loc> https://example.com/ch/</loc>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="jp"
　　　　href="https://example.com/"/>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="en"
　　　　href="https://example.com/en/"/>
　<xhtml:link
　　　　rel="alternate"
　　　　hreflang="zh-Hans"
　　　　href=" https://example.com/ch/"/>
</url>
</urlset>
```
