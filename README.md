## svelte-intl

[![Build Status](https://travis-ci.org/Panya/svelte-intl.svg?branch=master)](https://travis-ci.org/Panya/svelte-intl)
[![NPM Version](https://img.shields.io/npm/v/svelte-intl.svg)](https://npm.im/svelte-intl)
[![Package Size](https://img.shields.io/bundlephobia/minzip/svelte-intl.svg)](https://bundlephobia.com/result?p=svelte-intl@latest)

Internationalize your Svelte apps using [format-message](https://github.com/format-message/format-message).

```js
import { intl } from 'svelte-intl';
import { Store } from 'svelte';

const store = intl(new Store());

store.intl.extendLocales({
  en: {
    hello: 'Hello, {name}'
  }
});

store.intl.setLocale('en');

const { _ } = store.get();

_('hello', { name: 'John' }) // => 'Hello, John'
```
