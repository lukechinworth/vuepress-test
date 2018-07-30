---
custom: Title
list:
    - one
    - two
    - three
sidebarDepth: 2
---

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
### Vue
* Md is compiled to html and then passed to vue-loader, so this works: {{ 3 + 4 }}
* You can access site metadata with the global `$page`: {{ $page }}
### Frontmatter
* Frontmatter for the current page is available on the `$page` object: {{ $page.frontmatter }}
* Set front matter with yaml at top of this markdown file
### Vue script and style
* Each markdown file is essentially a vue component, so you can do `script` and `style` per page
* So this can be styled with css: <span class="blue">blue text</span>
* Check out the console for js from this page

<script>
export default {
    mounted() {
        console.log('hello from home page')
    }
}
</script>

<style>
.blue {
    color: blue;
}
</style>

### Vue components
* Add components to `.vuepress/components`. These are registered as global, async components, like this block quote:

<BlockQuote citeUrl="http://example.com/" citeLabel="Author">
This is the quotation.

</BlockQuote>

### Navbar
* Nav bar links are specified in `.vuepress/config.js` at `themeConfig.nav`.
* Make a dropdown by nesting `items`

### Sidebar
* Specify pages to show in sidebar `themeConfig.sidebar` to config.
* Displays `h2` by default; specify `sidebarDepth` in frontmatter per page to display  `h3`
