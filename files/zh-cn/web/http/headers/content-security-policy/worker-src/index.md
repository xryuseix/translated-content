---
title: 'CSP: worker-src'
slug: Web/HTTP/Headers/Content-Security-Policy/worker-src
---

{{HTTPSidebar}}

The HTTP {{HTTPHeader("Content-Security-Policy")}} (CSP) **`worker-src`** directive specifies valid sources for {{domxref("Worker")}}, {{domxref("SharedWorker")}}, or {{domxref("ServiceWorker")}} scripts.

| CSP version    | 3                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Directive type | {{Glossary("Fetch directive")}}                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Fallback       | If this directive is absent, the user agent will first look for the {{CSP("child-src")}} directive, then the {{CSP("script-src")}} directive, then finally for the {{CSP("default-src")}} directive, when governing worker execution.Chrome 59 and higher skips the {{CSP("child-src")}} directive.Edge 17 skips the {{CSP("script-src")}} directive ([bug](https://developer.microsoft.com/en-us/microsoft-edge/platform/issues/17415478/)). |

## Syntax

One or more sources can be allowed for the `worker-src` policy:

```plain
Content-Security-Policy: worker-src <source>;
Content-Security-Policy: worker-src <source> <source>;
```

### Sources

{{page("Web/HTTP/Headers/Content-Security-Policy/connect-src", "Sources")}}

## Examples

### Violation cases

Given this CSP header:

```bash
Content-Security-Policy: worker-src https://example.com/
```

{{domxref("Worker")}}, {{domxref("SharedWorker")}}, {{domxref("ServiceWorker")}} are blocked and won't load:

```html
<script>
  var blockedWorker = new Worker("data:application/javascript,...");
  blockedWorker = new SharedWorker("https://not-example.com/");
  navigator.serviceWorker.register('https://not-example.com/sw.js');
</script>
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- {{HTTPHeader("Content-Security-Policy")}}
- [CSP for Web Workers](/zh-CN/docs/Web/API/Web_Workers_API/Using_web_workers#Content_security_policy)
- {{domxref("Worker")}}, {{domxref("SharedWorker")}}, {{domxref("ServiceWorker")}}
