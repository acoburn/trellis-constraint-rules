# trellis-constraint-rules

**Note**: this project has been merged into the core [Trellis repository](https://github.com/trellis-ldp/trellis).

A set of constraints on a trellis repository defining the rules that govern valid RDF.

These rules consist of:

  * No inappropriate LDP properties -- certain LDP properties can only be modified if the interaction model permits it
  * LDP Resource types cannot be set or changed by changing RDF triples
  * Certain properties (`acl:accessControl`, `ldp:membershipResource`) must be used with "in-domain" resources
  * Certain properties must have a range of a IRI and have a max-cardinality of 1 (`ldp:membershipResource`, `ldp:hasMemberRelation`, `ldp:isMemberOfRelation`, `ldp:insertedContentRelation`, `ldp:inbox`, `acl:accessControl`, `oa:annotationService`)

## Building

This code requires Java 8 and can be built with Gradle:

    ./gradlew install
