---
title: console.error()
slug: Web/API/console/error
page-type: web-api-instance-method
tags:
  - API
  - DOM
  - Debugging
  - Method
  - Web Development
  - web console
browser-compat: api.console.error
---

{{APIRef("Console API")}}

The **`console.error()`** method outputs an error message to the Web console.

{{AvailableInWorkers}}

## Syntax

```js
error(obj1)
error(obj1, /* …, */ objN)
error(msg)
error(msg, subst1, /* …, */ substN)
```

### Parameters

- `obj1` … `objN`
  - : A list of JavaScript objects to output. The string representations of each of
    these objects are appended together in the order listed and output.
- `msg`
  - : A JavaScript string containing zero or more substitution strings.
- `subst1` … `substN`
  - : JavaScript objects with which to replace substitution strings within
    `msg`. This gives you additional control over the format of the output.

See [Outputting text to the console](/en-US/docs/Web/API/console#outputting_text_to_the_console) in the documentation of {{domxref("console")}} for
details.

### Return value

None ({{jsxref("undefined")}}).

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- [MSDN: Using the F12 Tools Console to View Errors and Status](https://docs.microsoft.com/previous-versions/windows/internet-explorer/ie-developer/samples/gg589530(v=vs.85))
- [Chrome Developer Tools: Using the Console](https://developer.chrome.com/docs/devtools/console/api/#error)
