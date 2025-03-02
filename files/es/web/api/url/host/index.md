---
title: Estabilidad
slug: Web/API/URL/Host
translation_of: Web/API/URL/host
---

{{ApiRef("URL API")}}

The **`host`** property of the {{domxref("URL")}} interface is a {{domxref("USVString")}} containing the host, that is the {{domxref("URL.hostname", "hostname")}}, and then, if the {{glossary("port")}} of the URL is nonempty, a `':'`, followed by the {{domxref("URL.port", "port")}} of the URL.

{{AvailableInWorkers}}

## Syntax

```
const host = url.host
url.host = newHost
```

### Value

A {{domxref("USVString")}}.

## Examples

```js
let url = new URL('https://developer.mozilla.org/en-US/docs/Web/API/URL/host');
console.log(url.host); // "developer.mozilla.org"

url = new URL('https://developer.mozilla.org:443/en-US/docs/Web/API/URL/host');
console.log(url.host); // "developer.mozilla.org"
// The port number is not included because 443 is the scheme's default port

url = new URL('https://developer.mozilla.org:4097/en-US/docs/Web/API/URL/host');
console.log(url.host); // "developer.mozilla.org:4097"
```

## Specifications

| Specification                                                    | Status               | Comment            |
| ---------------------------------------------------------------- | -------------------- | ------------------ |
| {{SpecName('URL', '#dom-url-host', 'URL.host')}} | {{Spec2('URL')}} | Initial definition |

## Browser compatibility

{{Compat("api.URL.host")}}

## See also

- The {{domxref("URL")}} interface it belongs to.
