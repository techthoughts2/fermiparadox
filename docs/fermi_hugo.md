# Site Creation Doc

## Synopsis

This is a quick reference document that shows how this site was built.

## Prerequisites

* Read [Getting Started - Installing Hugo](https://gohugo.io/getting-started/installing)
* [Choose a Theme](https://themes.gohugo.io)
* [Create and activate an Amazon Web Services account](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/)
* Create a new repository on GitHub

## Process

*Note: This process outline is based around using Windows as the primary workstation*

1. Install hugo *(many ways to do this, but the easiest is chocolatey)*
    ```choco install hugo -confirm```
2. Navigate to the directory where you'll be working with your new hugo site
    ```cd C:\dev\site```
3. Create a New Site
    ```hugo new site quickstart```
4. Add your theme to the themes folder
    * *Your themes documentation will likely have further install guidance on this*
5. Add some content. You can add single files with:
    ```hugo new <SECTIONNAME>\<FILENAME>.<FORMAT>```
6. Start the Hugo server
    ```hugo server -D```
7. Navigate your browser to: **http://localhost:1313/**
8. Commit site to GitHub repo
9. [Build your hugo site using AWS Amplify](https://gohugo.io/hosting-and-deployment/hosting-on-aws-amplify/)

## Useful Hugo Commands

```
hugo --help
hugo new site quickstart
hugo new <SECTIONNAME>\<FILENAME>.<FORMAT>
hugo new posts/my-first-post.md
hugo server -D
hugo server -D -s site/
hugo -s
hugo -s site
```

## Hugo Tips

* [How to create a static home page](https://timhilliard.com/blog/static-home-page-in-hugo/)
* Get rid of extra bullet point in table of contents:
    ```
    {{ .TableOfContents | replaceRE "<nav([^>]*)>\\s*<ul>\\s*<li>([\\s\\S]+)</li>\\s*</ul>\\s*</nav>" "<nav$1>$2</nav>" | safeHTML }}
    ```
* Only include a Table of Contents on certain pages:
  * Edit your ```/themes/layouts/_default/<desiredfile>```

        ```
        {{ if .Params.toc }}
        {{ .TableOfContents | replaceRE "<nav([^>]*)>\\s*<ul>\\s*<li>([\\s\\S]+)</li>\\s*</ul>\\s*</nav>" "<nav$1>$2</nav>" | safeHTML }}
        {{ end }}
        ```
  * On each content page add: ```toc: true``` if you want a ToC
* ```/themes/layouts/_default``` files can be used to influence the look and feel of your site

## Themes

**Main Theme**: [vanilla-bootstrap-hugo-theme](https://themes.gohugo.io/vanilla-bootstrap-hugo-theme/)

Hugo Themes that were considered:

* [hugo-h5bp](https://themes.gohugo.io/hugo-h5bp/)
* [whiteplain](https://themes.gohugo.io/whiteplain/)
* [minimal-bootstrap-hugo-theme](https://themes.gohugo.io/minimal-bootstrap-hugo-theme/)
* [hermit](https://themes.gohugo.io/hermit/)
* [hugo-theme-basic](https://themes.gohugo.io/hugo-theme-basic/)
* [beautifulhugo](https://themes.gohugo.io/beautifulhugo/)
* [hugo-theme-yinyang](https://themes.gohugo.io/hugo-theme-yinyang/)
* [air](https://themes.gohugo.io/air/)
* [hugo-primer](https://themes.gohugo.io/hugo-primer/)