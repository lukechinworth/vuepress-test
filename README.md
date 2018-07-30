# Home page
This is the home page of your vuepress site.
Go nuts with markdown.
```js
'example'.slice();
```
## Vuepress notes
### Installation
* Global install for standalone project (e.g. solid book)
* Alternative is local install inside existing project (e.g. docs for a web project)
* 1305 packages. Holy shnikes!
### Dev
* `vuepress dev` serves at http://localhost:8080/
* Hot reload with updates
* Add more dirs and READMEs, e.g. /tv/README.md
* View at /tv/ (trailing slash required)
### Config
* Add .vuepress/config.js
* Config title appears in header
* Config description is meta
* Webpage title is vuepress page title joined with config title
### Deploy
* `vuepress build` builds to `.vuepress/dist` by default
* Simply serve as static site, e.g. on github pages, https://lukechinworth.github.io/vuepress-test/built-site/
### Links
* Link is the [TV page](/tv/) will be updated with url base automatically
* Links do not refresh. Front end is single page app.
* `vuepress dev` will serve from base url config http://localhost:8080/vuepress-test/built-site/
