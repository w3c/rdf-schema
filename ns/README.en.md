# English vocabulary annotations

These three files provide English annotations for all 87 terms
in the base RDF (32), RDFS (16) and XML Schema
(39) vocabulary files. Every source label, comment, vocabulary title
and description has a counterpart in this language.

The separate files follow the [review feedback on PR #76](https://github.com/w3c/rdf-schema/pull/76#issuecomment-5890689702).
The annotations cover every term in these three source files.
Source revision: `e8eebcdcee2265735ab1058d1cc7a2b365a70567`; source files: `ns/rdf.ttl`, `ns/rdfs.ttl`, `ns/rdf-xsd.ttl`.

Load `rdf.en.ttl`, `rdfs.en.ttl` and `rdf-xsd.en.ttl` alongside their
corresponding base files in `ns/`. These are supplementary annotation graphs.
Schema axioms, links, dates and deprecation flags remain in the base files.
All subjects use the original namespace IRIs.

`rdfs:label` supplies a language-tagged name for consumers using RDFS.
`skos:prefLabel` supplies one preferred, readable name per term in this language.
`rdfs:comment` supplies the description. Vocabulary titles and descriptions use
`dcterms:title` and `dcterms:description`. SKOS labeling properties can label
resources without declaring them `skos:Concept`; see the
[SKOS reference](https://www.w3.org/TR/skos-reference/#labels).

English `rdfs:label` and `rdfs:comment` strings are copied verbatim from the base
files and given `@en` tags here. Proposed `skos:prefLabel` strings expand technical
names where useful and use sentence case.

Existing vocabulary files and specification documents remain unchanged. This
proposal adds no content negotiation or publication configuration. The choice of
preferred labels and whether to retain both labeling predicates are open for review.
The comments translate existing text rather than revising datatype definitions.
