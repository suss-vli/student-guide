
# Try asciidoc

https://asciidoc.org/#try

# Requirement
- [pandoc](https://pandoc.org)
- [asciidoctor](https://asciidoctor.org)

# Convert docx to adoc using pandoc

> we should aim for a naming convention with no space and all down case. See name.md

`pandoc Student\ Guide\ for\ Virtual\ Lab\ WorkSpace\ v.1.0.docx -f docx -t asciidoc --wrap=none --markdown-headings=atx --extract-media=extracted-media  -o src/output.adoc`


## convert to epub or mobi or k8
> require asciidoctor-epub3

src: https://docs.asciidoctor.org/epub3-converter/latest/

`asciidoctor-epub3 -D output -a ebook-format=kf8 data/samples/sample-book.adoc`

# convert to html 

`asciidoctor my-document.adoc`

# convert adoc to markdown

`asciidoc -b docbook yourfile.adoc`\
`pandoc -f docbook -t markdown_strict yourfile.xml -o yourfile.md`

https://karinavarela.me/2020/05/06/converting-asciidoc-to-markdown/


# just copy and pasting from another student guide readme
TODO: remember to remove this
# insert the command to convert adoc to word

```
INPUT_ADOC=my_input_file.adoc
asciidoctor --backend docbook --out-file - $INPUT_ADOC| \
pandoc --from docbook --to docx --output $INPUT_ADOC.docx
```
> Src: https://rmoff.net/2020/04/16/converting-from-asciidoc-to-google-docs-and-ms-word/


# command to convert word to adoc
```
pandoc X.docx -f docx -t asciidoc --wrap=none --markdown-headings=atx --extract-media=extracted-media -o src/output.adoc
```
# command to convert adoc to html
```
asciidoctor X.adoc
```
