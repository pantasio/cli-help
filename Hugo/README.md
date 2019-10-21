hugo version
hugo new site <name-of-site>

hugo new post/first-post.md
hugo server

git init
git submodule add <url> themes/<name-theme>

git submodule add https://github.com/gkmngrgn/hugo-alageek-theme themes/alageek

cp themes/<name-theme>/exampleSite/* . -r

cp themes/alageek/exampleSite/* . -r

hugo undraft <url-post.md>

"""""""""""""
" make hugo generate HTML
change config.toml
publishDir = "docs"
run hugo
"""""""""""""
