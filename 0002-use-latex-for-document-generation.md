# 2. Use LaTeX for document generation

Date: 2021-05-25

## Status

Accepted

## Context

To reduce copy/paste errors, we need to automatically generate common documents. A 3rd party tool is required in order to create pdf and/or word documents.

## Decision

We have decided to use LaTeX for document generation.

## Consequences

LaTeX is a very powerful engine, capable of producing many types of documents. This ensures that we can create all the document types that will be necessary in the future. It is also a well documented, portable, highly extensible, and very stable system.

On the downside, the LaTeX syntax is unusual. We expect that adding new types of document blocks will take longer than usual due to the need to research the format. However, this downside is estimated to be minimal at this point.

## Alternatives

We have looked at a number of alternatives to LaTeX.

### Pandoc + Markdown

Pandoc is a very capable tool for producing different types of documents. However, it has by design limitations in terms of layout and media. Moreover, it uses LaTeX under the hood for generating pdf documents. While easier to use than LaTeX, we are afraid its limitations will prove too restrictive in the future.

### xkhtmltopdf and other html to pdf tools

xkhtmltopdf is a very capable tool for producing pdf documents from html. This is an attractive option, since html is so well known and used.

However, html was not built for documents but for hypermedia. We feel that this gives a slight edge to LaTeX over html.

### Libraries that produce pdf files

We evaluated a few libraries that can be used to produce pdf files directly. While convenient for programming, their downside relates to the need for understanding the pdf format. We also are not sure whether we will use exclusively pdf files; it's likely we will need to create word documents and perhaps slides as well. LaTeX is overall more capable of these features than any specialized pdf library.
