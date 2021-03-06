# hexo-filter-nofollow-with-goto

[![npm version](https://badge.fury.io/js/hexo-filter-nofollow-with-goto.svg)](https://www.npmjs.com/package/hexo-filter-nofollow-with-goto)
[![npm license](https://img.shields.io/npm/l/hexo-filter-nofollow-with-goto)](./LICENSE)
<!-- [![travis status](https://api.travis-ci.com/hexojs/hexo-filter-nofollow.svg?branch=master)](https://travis-ci.com/hexojs/hexo-filter-nofollow) -->
![npm download](https://img.shields.io/npm/dt/hexo-filter-nofollow-with-goto)

Fork from hexo-filter-nofollow.

Add nofollow attribute to all external links, or convert all external links to internal links automatically.

`hexo-filter-nofollow` add `rel="noopener external nofollow noreferrer"` to all external links for security, privacy and SEO. [Read more](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types).

## Installations

```bash
$ npm i hexo-filter-nofollow-with-goto --save
```

## Options

```yaml
nofollow:
  enable: true
  field: site
  exclude:
    - 'exclude1.com'
    - 'exclude2.com'
  goto: 
    - enable: false,
    - prefix: '/goto/?u='
```

- **enable** - Enable the plugin. Default value is `true`.
- **field** - The scope you want the plugin to proceed, can be 'site' or 'post'. Default value is `site`.
  - 'post' - Only add nofollow attribute to external links in your post content
  - 'site' - Add nofollow attribute to external links of whole sites
- **exclude** - Exclude hostname. Specify subdomain when applicable, including `www`.
  - 'exclude1.com' does not apply to `www.exclude1.com` nor `en.exclude1.com`.
- **goto** 
  - 'enable' - Convert all external links to internal links automatically. Default value is `false`.
  - 'prefix' - the internal link's prefix, default value is `'/goto/?u='`.
