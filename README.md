<div align="center" margin="0 auto 20px">
  <h1>svelte-copyright</h1>
  <p style="font-style: italic;">© A Svelte component to format and display a copyright notice.</p>
  <div>
    <a href='https://travis-ci.com/github/himynameisdave/svelte-copyright'>
        <img src="https://travis-ci.com/himynameisdave/svelte-copyright.svg?branch=master" alt="Travis Badge" />
    </a>
    <a href="https://packagephobia.now.sh/result?p=svelte-copyright">
        <img src="https://packagephobia.now.sh/badge?p=svelte-copyright" alt="Install size" />
    </a>
    <a href="https://bundlephobia.com/result?p=svelte-copyright">
        <img src="https://img.shields.io/bundlephobia/min/svelte-copyright.svg" alt="Bundle size (minified)" />
    </a>
  </div>
</div>

---

A [Svelte](https://svelte.dev/) component to format and display a copyright notice.

<!-- [**Try me on CodeSandbox!**](https://codesandbox.io/s/svelte-flex-5s45y) -->

### Installation

This package is available on NPM, and you can install it with `npm` or `yarn`:

```
npm install svelte-copyright

yarn add svelte-copyright
```

### Usage

Import the `Copyright` component and use it in your Svelte project.

```svelte
<script>
  import Copyright from 'svelte-copyright';
</script>

<footer>
  <Copyright>
    Dave Lunny
  </Copyright>
</footer>
```

This will output HTML which looks something like this:

```html
<footer>
  <span>© Copyright 2020 Dave Lunny</span>
</footer>
```

#### Props

All props are optional (as they all have default values).

**Prop** | **Possible Values** | **Default Value** | **Description**
---|---|---|---
`date` | [RFC2822/ISO8601](https://tools.ietf.org/html/rfc2822#page-14) date string | `Date.now()` | Date for the copyright year.
`format` | `'numeric'` \| `'2-digit'` | `'numeric'` | Format for the copyright year.
`position` | `'pre'` \| `'post'`  | `'pre'` | Position of the Copyright relative to the contents you provide.

**Additional Props**

Note that any additonal props will be spread onto the component. This allows you to do things like provide a custom `class` name to your component.

```svelte
<Copyright class="custom-copyright">
  Dave Lunny
</Copyright>

<style>
  :global(.custom-copyright) {
    color: lime;
  }
</style>
```

### Contributing

Feel free to [file an issue](https://github.com/himynameisdave/svelte-copyright/issues/new) or open a pull request. Ensure that you add tests for any new functionality.

### Inspiration

This was inspired by [`react-copyright`](https://github.com/jasonbellamy/react-copyright) by [Jason Bellamy](https://github.com/jasonbellamy).

---

_✌️ Built by [Dave Lunny](http://himynameisdave.com)._
