# Convert docx to adoc using pandoc

> we should aim for a naming convention with no space and all down case. See name.md

pandoc Student\ Guide\ for\ Virtual\ Lab\ WorkSpace\ v.1.0.docx -f docx -t asciidoc --wrap=none --markdown-headings=atx --extract-media=extracted-media  -o src/output.adoc src/output.epub


## convert to epub or mobi or k8
> require asciidoctor-epub3

src: https://docs.asciidoctor.org/epub3-converter/latest/

asciidoctor-epub3 -D output -a ebook-format=kf8 data/samples/sample-book.adoc

# convert to html 

asciidoctor my-document.adoc
