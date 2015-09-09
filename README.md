# chicago-legislation-examples

## Resolutions
We're currently drafting example XML documents for Chicago resolutions.  The drafts are based on [Akoma Ntoso](http://www.akomantoso.org/).

The PDF versions can be found in the `resolutions/pdf` directory and their xml representations are in the `resolutions/xml` directory, matching based on name.

**The only current version in Akoma Ntoso is below**

ie. `resolutions/pdf/R2015-232.pdf` -> `resolutions/xml/R2015-232.xml`

The current top-level document structure for resolutions looks like:

```
<akomaNtoso>
  <metadata>...</metadata> //Currently uses the dublinCore standard for document meta info
  <preface>...</preface> //This hold the cover sheet information from the resolution pdfs.
  <preamble>...</preamble> //This holds the "whereas" clauses
  <body>...</body> //This holds the "Be it resolved" / "Be it further resolved" clauses
  <conclusions>...</conclusions> //This hold the signatures
</akomaNtoso>

```

TODO:
* How to handle `meta` correctly.  Currently just using `dublinCore` standards.
* How to handle the `coverPage` element
* All Akoma Ntoso versioning-specific meta (currently marked as required by the schema)
* Add document number to the preface ( and metadata ?)