https://gohugo.io/getting-started/installing
choco install hugo -confirm
hugo new site quickstart


1. Download a theme into the same-named folder.
   Choose a theme from https://themes.gohugo.io/, or
   create your own with the "hugo new theme <THEMENAME>" command.
2. Perhaps you want to add some content. You can add single files
   with "hugo new <SECTIONNAME>\<FILENAME>.<FORMAT>".
3. Start the built-in live server via "hugo server".

## Themes
https://themes.gohugo.io/vanilla-bootstrap-hugo-theme/
https://themes.gohugo.io/hugo-h5bp/
https://themes.gohugo.io/whiteplain/
https://themes.gohugo.io/minimal-bootstrap-hugo-theme/
https://themes.gohugo.io/minimal-bootstrap-hugo-theme/
https://themes.gohugo.io/hermit/
https://themes.gohugo.io/hugo-theme-basic/
https://themes.gohugo.io/beautifulhugo/
https://themes.gohugo.io/hugo-theme-yinyang/
https://themes.gohugo.io/air/
https://themes.gohugo.io/hugo-primer/


hugo new posts/my-first-post.md
hugo server -D

https://timhilliard.com/blog/static-home-page-in-hugo/

hermit
hugo-theme-basic
minimal-bootstrap-hugo-theme
vanilla-bootstrap-hugo-theme

https://tachyons.io/components/

https://getbootstrap.com/docs/4.3/content/tables/


{{ .TableOfContents | replaceRE "<nav([^>]*)>\\s*<ul>\\s*<li>([\\s\\S]+)</li>\\s*</ul>\\s*</nav>" "<nav$1>$2</nav>" | safeHTML }}