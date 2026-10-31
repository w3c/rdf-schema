# Chinese (Simplified) vocabulary annotations

These three files provide Chinese (Simplified) annotations for all 87 terms
in the base RDF (32), RDFS (16), and XML Schema (39) vocabulary
files. Every source label, comment, vocabulary title, and
description has a counterpart in this language.

The separate files follow the [review feedback on PR #76](https://github.com/w3c/rdf-schema/pull/76#issuecomment-5890689702)
and the file organization of [French PR #88](https://github.com/w3c/rdf-schema/pull/88).
Related tracking issue: [#90](https://github.com/w3c/rdf-schema/issues/90).
Source revision: `476ad2dc997a9f6085204bbdead2b14cee511d70`; source files:
`ns/rdf.ttl`, `ns/rdfs.ttl`, `ns/rdf-xsd.ttl`.
These base files are unchanged from the revision used by the existing language PRs.
English annotations are copied without textual changes from
[`vocabulary-en` at `aff0700`](https://github.com/w3c/rdf-schema/tree/aff07007e0a618b6417be205bfb9dd4debe4e614/ns).
The supplementary annotation structure follows
[`vocabulary-fr` at `6c5e527`](https://github.com/w3c/rdf-schema/tree/6c5e5276bc9af0a3102cd15aacc5ed2398e80a1d/ns).

Load `rdf.zh.ttl`, `rdfs.zh.ttl`, and `rdf-xsd.zh.ttl` alongside their
corresponding base files in `ns/`. These are supplementary annotation graphs.
Schema axioms, links, dates, and deprecation flags remain in the base files.
All subjects use the original namespace IRIs.

`rdfs:label` supplies a language-tagged name for consumers using RDFS.
`skos:prefLabel` supplies one preferred, readable name per term in this language.
`rdfs:comment` supplies the description, again in this language. Vocabulary
titles and descriptions use `dcterms:title` and `dcterms:description`. SKOS
labeling properties can label resources without declaring them `skos:Concept`;
see the [SKOS reference](https://www.w3.org/TR/skos-reference/#labels).

Translated `rdfs:label` and `skos:prefLabel` strings agree. The labels and comments
use `@zh` tags. Class and datatype labels are nouns. Relational labels retain
the direction of the source relationship, using this language's word order.
Technical identifiers, numeric bounds, example literals, and floating-point
regular expressions retain their source form.
The `@zh` tag follows the language-only file naming convention used by the
other language PRs. The Chinese text uses Simplified Chinese characters.

Each file also includes all annotations from its English counterpart:
labels, comments, vocabulary titles, and descriptions tagged `@en`, together with
the English preferred labels. English text matches the English annotation files,
including the added comma after `i/10^n` in the `xsd:decimal` comment.
`skos:altLabel` retains the original English source name when it differs from the
English `skos:prefLabel`. A source name is not added as an alternative if it is
already the English preferred label. Each term has one preferred label per language.

For consistency with the existing language PRs, the four `rdf:version-*`
resources retain their version strings as labels tagged `@zh` and `@en`.
The version strings themselves are unchanged. The discussion of whether version
labels should instead remain untagged is still open in #90.

Terminology was checked against the contributor's existing
[RDF Schema translation](https://github.com/JinDX/htmlspecs.com/blob/2126ff78e6625ed19687b4f407325f9651206050/rdf12-schema/index.html)
and [RDF Concepts translation](https://github.com/JinDX/htmlspecs.com/blob/2126ff78e6625ed19687b4f407325f9651206050/rdf12-concepts/index.html).
Examples: resource → 资源; property → 属性; literal → 字面量; proposition → 命题; reification → 具体化; lexical form → 词法形式; value space → 值空间.

These initial translations were prepared with OpenAI GPT-6 (Codex) assistance.
They have been checked against the English comments and the terminology sources
above; no independent native-speaker or second-model review is claimed.
Review by fluent speakers is welcome.

Existing vocabulary files and specification documents remain unchanged. This
proposal adds no content negotiation or publication configuration. The choice of
preferred labels and whether to retain both labeling predicates are open for review.
The comments translate existing text rather than revising datatype definitions.
