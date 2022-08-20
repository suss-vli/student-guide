# Convert docx to adoc using pandoc

pandoc input.docx -f docx -t asciidoc --wrap=none --markdown-headings=atx --extract-media=extracted-media  -o output2.adoc