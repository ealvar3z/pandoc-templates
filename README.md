# easy pandoc templates

A collection of portable pandoc templates with no dependencies

requires [pandoc](https://pandoc.org/installing.html)

#### Screenshot
![](https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/samples/screenshots/elegant_bootstrap_menu.png)

[Live Demo](http://htmlpreview.github.io/?https://github.com/ealvar3z/easy-pandoc-templates/blob/master/samples/elegant_bootstrap_menu_sample.html)

## quick start

#### install

``` bash
# Clones repo to /tmp and copies templates to ~/.pandoc/templates

curl 'https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/copy_templates.sh' | bash
```

#### usage

``` bash
# pandoc source.md -o destination.html --template=template_name.html

pandoc 'https://raw.githubusercontent.com/jgm/pandoc/master/MANUAL.txt' -f markdown -o sample.html --template=easy_template.html --toc
```

## usage

Use it just like any other pandoc template, but don't worry about where the extraneous files are (like css, js, etc)

``` bash
# pandoc source.md -o destination.html --template=template_name.html

pandoc source.md -o destination.html --template=easy_template.html
```

Pandoc will look in `~/.pandoc/templates` for files with the template name.

Don't forget to add `--toc` if you want a table of contents.

If you want the document to work offline, add the `--standalone` flag to pull all of the headers
into the final document. See [the pandoc manual for more info](https://pandoc.org/MANUAL.html)

## installation

To install all the templates:

``` bash
# Clones repo to /tmp and copies templates to ~/.pandoc/templates

curl 'https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/remote_install.sh' | bash
```

To install a single template, copy the given template to `~/.pandoc/templates`.

``` bash
# curl '<url to raw html template in this repo>' > ~/.pandoc/templates/<template name>

curl 'https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/html/easy_template.html' > ~/.pandoc/templates/easy_template.html
```

## gallery

### elegant bootstrap

A nice looking responsive template using bootstrap. Can create a nice table of contents menu

![](https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/samples/screenshots/elegant_bootstrap_menu.png)

[Live Demo](http://htmlpreview.github.io/?https://github.com/ealvar3z/easy-pandoc-templates/blob/master/samples/elegant_bootstrap_menu_sample.html)


### uikit

![](https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/samples/screenshots/uikit.png)

[Live Demo](http://htmlpreview.github.io/?https://github.com/ealvar3z/easy-pandoc-templates/blob/master/samples/uikit_sample.html)

### bootstrap

A nice looking responsive template using bootstrap. Can create a nice table of contents menu

![](https://raw.githubusercontent.com/ealvar3z/easy-pandoc-templates/master/samples/screenshots/bootstrap_menu.png)

[Live Demo](http://htmlpreview.github.io/?https://github.com/ealvar3z/easy-pandoc-templates/blob/master/samples/bootstrap_menu.html)

## extras

### vim

Want to preview your markdown file instantly in the browser? Add the following line to your .vimrc to bind Ctrl-m to compile vim's current file and display it in firefox.
Feel free to change the template as you please

``` vimscript
# For firefox
noremap <C-M> :! pandoc '%:p' -o /tmp/'%:p:t'.html --template=easy_template.html --toc && firefox /tmp/'%:p:t'.html &<CR><CR>

# For chrome
noremap <C-M> :! pandoc '%:p' -o /tmp/'%:p:t'.html --template=easy_template.html --toc && google-chrome /tmp/'%:p:t'.html &<CR><CR>
```
