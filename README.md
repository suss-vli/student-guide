# Convert docx to adoc using pandoc

> we should aim for a naming convention with no space and all down case. See NAME.md

pandoc Student\ Guide\ for\ Virtual\ Lab\ WorkSpace\ v.1.0.docx -f docx -t asciidoc --wrap=none --markdown-headings=atx --extract-media=extracted-media  -o src/output.adoc