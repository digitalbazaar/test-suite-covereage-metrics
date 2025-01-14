# Test Suite Coverage Metrics
## vc-di-eddsa-test-suite
### Summary of normative statements coverage

| Count (Suite) | Count (Spec) | Matches | Unmatched (Suite) | Unmatched (Spec) |
| ------- | ------- | ------- | ------- | ------- |
| 60 | 57 | 21 |  39 |  36 |

### Details
#### Test Suite Statements
```json
[
  "When expressing a data integrity proof on an object, a proof property MUST be used.",
  "If present (proof), its value MUST be either a single object, or an unordered set of objects.",
  "('proof.id') An optional identifier for the proof, which MUST be a URL.",
  "The specific type of proof MUST be specified as a string that maps to a URL.",
  "The type property MUST contain the string DataIntegrityProof.",
  "The proofValue property MUST be used, as specified in 2.1 Proofs.",
  "If the proof type is DataIntegrityProof, cryptosuite MUST be specified; otherwise, cryptosuite MAY be specified.",
  "If specified (proof.cryptosuite), its value MUST be a string.",
  "A verification method is the means and information needed to verify the proof. If included, the value MUST be a string that maps to a [URL].",
  "The reason the proof was created ('proof.proofPurpose') MUST be specified as a string that maps to a URL.",
  "('proof.proofValue') A string value that expresses base-encoded binary data necessary to verify the digital proof using the verificationMethod specified. The value MUST use a header and encoding as described in Section 2.4 Multibase of the Controller Documents 1.0 specification to express the binary data.",
  "Cryptographic suite designers MUST use mandatory proof value properties defined in Section 2.1 Proofs, and MAY define other properties specific to their cryptographic suite.",
  "Implementations that use JSON-LD processing, such as RDF Dataset Canonicalization [RDF-CANON], MUST throw an error, which SHOULD be DATA_LOSS_DETECTION_ERROR, when data is dropped by a JSON-LD processor, such as when an undefined term is detected in an input document.",
  "If the algorithm produces an error, the error MUST be propagated and SHOULD convey the error type.",
  "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite.",
  "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite. If the processing environment supports subtypes of string, the type of the cryptosuite value MUST be the https://w3id.org/security#cryptosuiteString subtype of string.",
  "When deserializing to RDF, implementations MUST ensure that the base URL is set to null.",
  "Conforming processors MUST produce errors when non-conforming documents are consumed.",
  "If either securedDocument is not a map or securedDocument.proof is not a map, an error MUST be raised and SHOULD convey an error type of PARSING_ERROR.",
  "If one or more of proof.type, proof.verificationMethod, and proof.proofPurpose does not exist, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR",
  "The type property MUST contain the string DataIntegrityProof.",
  "If expectedProofPurpose was given, and it does not match proof.proofPurpose, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "The proofValue property MUST be used, as specified in 2.1 Proofs.",
  "('proof.proofValue') A string value that contains the base-encoded binary data necessary to verify the digital proof using the verificationMethod specified. The contents of the value MUST be expressed with a header and encoding as described in Section 2.4 Multibase of the Controller Documents 1.0 specification.",
  "Implementations that use JSON-LD processing, such as RDF Dataset Canonicalization [RDF-CANON], MUST throw an error, which SHOULD be DATA_LOSS_DETECTION_ERROR, when data is dropped by a JSON-LD processor, such as when an undefined term is detected in an input document.",
  "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite. If the processing environment supports subtypes of string, the type of the cryptosuite value MUST be the https://w3id.org/security#cryptosuiteString subtype of string.",
  "An OPTIONAL string value (proof.previousProof) or unordered list of string values. Each value identifies another data integrity proof that MUST verify before the current proof is processed.",
  "If an unordered list (proof), all referenced proofs in the array MUST verify.",
  "If a proof with id equal to previousProof does not exist in allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "If any element of previousProof list has an id attribute that does not match the id attribute of any element of allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "Each value identifies another data integrity proof, all of which MUST also verify for the current proof to be considered verified",
  "The type property MUST be DataIntegrityProof.",
  "The cryptosuite property of the proof MUST be eddsa-rdfc-2022 or eddsa-jcs-2022.",
  "The proofValue property of the proof MUST be a detached EdDSA signature produced according to [RFC8032], encoded using the base-58-btc header and alphabet as described in the Multibase section of Controller Documents 1.0.",
  "The publicKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed.",
  "The secretKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed. (secretKeyMultibase)",
  "The type property MUST be DataIntegrityProof.",
  "The cryptosuite property of the proof MUST be eddsa-rdfc-2022 or eddsa-jcs-2022.",
  "The proofValue property of the proof MUST be a detached EdDSA signature produced according to [RFC8032], encoded using the base-58-btc header and alphabet as described in the Multibase section of Controller Documents 1.0.",
  "The publicKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed.",
  "The secretKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed. (secretKeyMultibase)",
  "The transformation options MUST contain a type identifier for the cryptographic suite (type) and a cryptosuite identifier (cryptosuite).",
  "Whenever this algorithm encodes strings, it MUST use UTF-8 encoding.",
  "If options.type is not set to the string DataIntegrityProof and options.cryptosuite is not set to the string eddsa-jcs-2022, an error MUST be raised that SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MUST contain a cryptosuite identifier (cryptosuite).",
  "If proofConfig.type is not set to DataIntegrityProof or proofConfig.cryptosuite is not set to eddsa-jcs-2022, an error MUST be raised that SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If proofConfig.created is set to a value that is not a valid [XMLSCHEMA11-2] datetime, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MAY contain a cryptosuite identifier (cryptosuite).",
  "The transformation options MUST contain a type identifier for the cryptographic suite (type) and a cryptosuite identifier  (cryptosuite).",
  "Whenever this algorithm encodes strings, it MUST use UTF-8 encoding.",
  "If options.type is not set to the string DataIntegrityProof and options.cryptosuite is not set to the string eddsa-rdfc-2022, an error MUST be raised that SHOULD convey an error type of PROOF_TRANSFORMATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MUST contain a cryptosuite identifier (cryptosuite).",
  "If proofConfig.type is not set to DataIntegrityProof and/or proofConfig.cryptosuite is not set to eddsa-rdfc-2022, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If proofConfig.created is present and set to a value that is not a valid [XMLSCHEMA11-2] datetime, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MAY contain a cryptosuite identifier (cryptosuite).",
  "An OPTIONAL string value (proof.previousProof) or unordered list of string values. Each value identifies another data integrity proof that MUST verify before the current proof is processed."
]
```
#### Specifications Statements
```json
[
  //! "The key words MAY, MUST, MUST NOT, OPTIONAL, and SHOULD in this document are to be interpreted as described in BCP 14 [RFC2119] [RFC8174] when, and only when, they appear in all capitals, as shown here.",
  "Conforming processors MUST produce errors when non-conforming documents are consumed.",
  // "When expressing a data integrity proof on an object, a proof property MUST be used",
  // "If present, its value MUST be either a single object, or an unordered set of objects, expressed using the properties below:",
  //! "An optional identifier for the proof, which MUST be a URL [URL], such as a UUID as a URN (urn:uuid:6a1676b8-b51f-11ed-937b-d76685a20ff5)",
  // "The specific type of proof MUST be specified as a string that maps to a URL [URL]",
  // "The reason the proof was created MUST be specified as a string that maps to a URL [URL]",
  "If included, the value MUST be a string that maps to a [URL]",
  // "If the proof type is DataIntegrityProof, cryptosuite MUST be specified; otherwise, cryptosuite MAY be specified",
  // "If specified, its value MUST be a string.",
  "The date and time the proof was created is OPTIONAL and, if included, MUST be specified as an [XMLSCHEMA11-2] dateTimeStamp string, either in Universal Coordinated Time (UTC), denoted by a Z at the end of the value, or with a time zone offset relative to UTC",
  "If present, it MUST be an [XMLSCHEMA11-2] dateTimeStamp string, either in Universal Coordinated Time (UTC), denoted by a Z at the end of the value, or with a time zone offset relative to UTC",
  "If specified, the associated value MUST be either a string, or an unordered set of strings",
  // "The value MUST use a header and encoding as described in Section 2.4 Multibase of the Controller Documents 1.0 specification to express the binary data",
  "If present, it MUST be a string value or an unordered list of string values",
  "Each value identifies another data integrity proof, all of which MUST also verify for the current proof to be considered verified",
  "If present, the digestMultibase value MUST be a single string value, or an list of string values, each of which is a Multibase-encoded Multihash value.",
  "Implementations that perform JSON-LD processing MUST treat the following JSON-LD context URLs as already resolved, where the resolved document matches the corresponding hash values below:",
  "Implementations that perform RDF processing MUST treat the JSON-LD serialization of the vocabulary URL as already dereferenced, where the dereferenced document matches the corresponding hash value below.",
  "Applications MUST use the algorithm in Section 4.6 Context Validation, or one that achieves equivalent protections, to validate contexts in a conforming secured document",
  "Context validation MUST be run after running the applicable algorithm in either Section 4.4 Verify Proof or Section 4.5 Verify Proof Sets and Chains.",
  "However, if an @context declaration is not included, extensions (such as the addition of new properties) related to this specification or corresponding cryptosuites MUST NOT be made.",
  "Implementations that use JSON-LD processing, such as RDF Dataset Canonicalization [RDF-CANON], MUST throw an error, which SHOULD be DATA_LOSS_DETECTION_ERROR, when data is dropped by a JSON-LD processor, such as when an undefined term is detected in an input document.",
  "When deserializing to RDF, implementations MUST ensure that the base URL is set to null.",
  //! "The specification MUST be published as a human-readable document at a URL.",
  //! "The specification MUST identify a cryptographic suite type and any parameters that can be used with the suite.",
  //! "The specification MUST detail the transformation algorithms (if any), parameters, and other necessary details, used to modify input data into the data to be protected.",
  //! "The specification MUST detail the hashing algorithms parameters, and other necessary details used to perform cryptographic hashing to the data to be protected.",
  //! "The specification MUST detail the proof serialization algorithms, parameters, and other necessary details used to perform cryptographic protection of the data.",
  //! "The specification MUST detail the proof verification algorithms, parameters, and other necessary details used to perform cryptographic verification of the data.",
  //! "The specification MUST define a data integrity cryptographic suite instantiation algorithm that accepts a set of options (map options) and returns a cryptosuite instance (struct cryptosuite)",
  //! "The specification MUST detail any known resource starvation attack that can occur in an algorithm and provide testable mitigations against each attack.",
  //! "The specification MUST contain a Security Considerations section detailing security considerations specific to the cryptographic suite.",
  //! "The specification MUST contain a Privacy Considerations section detailing privacy considerations specific to the cryptographic suite.",
  //! "The JSON-LD context associated with the cryptographic suite MUST have its terms protected from unsafe redefinition, by use of the @protected keyword.",
  "The type property MUST contain the string DataIntegrityProof.",
  "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite",
  "If the processing environment supports string subtypes, the subtype of the cryptosuite value MUST be the https://w3id.org/security#cryptosuiteString subtype.",
  "The proofValue property MUST be used, as specified in Section 2.1 Proofs.",
  "Cryptographic suite designers MUST use mandatory proof value properties defined in Section 2.1 Proofs, and MAY define other properties specific to their cryptographic suite.",
  "Whenever this algorithm encodes strings, it MUST use UTF-8 encoding.",
  "If the algorithm produces an error, the error MUST be propagated and SHOULD convey the error type.",
  "If one or more of the proof.type, proof.verificationMethod, and proof.proofPurpose values is not set, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If options has a non-null domain item, it MUST be equal to proof.domain or an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If options has a non-null challenge item, it MUST be equal to proof.challenge or an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If a proof with id equal to previousProof does not exist in allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If any element of previousProof list has an id attribute that does not match the id attribute of any element of allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "When a step says 'an error MUST be raised', it means that a verification result MUST be returned with a verified value of false and a non-empty errors list.",
  "If either securedDocument is not a map or securedDocument.proof is not a map, an error MUST be raised and SHOULD convey an error type of PARSING_ERROR.",
  "If one or more of proof.type, proof.verificationMethod, and proof.proofPurpose does not exist, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "If expectedProofPurpose was given, and it does not match proof.proofPurpose, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "If domain was given, and it does not contain the same strings as proof.domain (treating a single string as a set containing just that string), an error MUST be raised and SHOULD convey an error type of INVALID_DOMAIN_ERROR.",
  "If challenge was given, and it does not match proof.challenge, an error MUST be raised and SHOULD convey an error type of INVALID_CHALLENGE_ERROR.",
  "If a proof with id value equal to the value of previousProof does not exist in allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR",
  "If any element of previousProof list has an id attribute value that does not match the id attribute value of any element of allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "The type value of the error object MUST be a URL that starts with the value https://w3id.org/security# and ends with the value in the section listed below.",
  //! "The code value MUST be the integer code described in the table below (in parentheses, beside the type name)."
]
```
#### Matched Statements
```json
[
  [
    "Conforming processors MUST produce errors when non-conforming documents are consumed.",
    "Conforming processors MUST produce errors when non-conforming documents are consumed."
  ],
  [
    "If present, its value MUST be either a single object, or an unordered set of objects, expressed using the properties below:",
    "If present (proof), its value MUST be either a single object, or an unordered set of objects."
  ],
  [
    "The specific type of proof MUST be specified as a string that maps to a URL [URL]",
    "The specific type of proof MUST be specified as a string that maps to a URL."
  ],
  [
    "If the proof type is DataIntegrityProof, cryptosuite MUST be specified; otherwise, cryptosuite MAY be specified",
    "If the proof type is DataIntegrityProof, cryptosuite MUST be specified; otherwise, cryptosuite MAY be specified."
  ],
  [
    "Each value identifies another data integrity proof, all of which MUST also verify for the current proof to be considered verified",
    "Each value identifies another data integrity proof, all of which MUST also verify for the current proof to be considered verified"
  ],
  [
    "Implementations that use JSON-LD processing, such as RDF Dataset Canonicalization [RDF-CANON], MUST throw an error, which SHOULD be DATA_LOSS_DETECTION_ERROR, when data is dropped by a JSON-LD processor, such as when an undefined term is detected in an input document.",
    "Implementations that use JSON-LD processing, such as RDF Dataset Canonicalization [RDF-CANON], MUST throw an error, which SHOULD be DATA_LOSS_DETECTION_ERROR, when data is dropped by a JSON-LD processor, such as when an undefined term is detected in an input document."
  ],
  [
    "The type property MUST contain the string DataIntegrityProof.",
    "The type property MUST contain the string DataIntegrityProof."
  ],
  [
    "The proofValue property MUST be used, as specified in Section 2.1 Proofs.",
    "The proofValue property MUST be used, as specified in 2.1 Proofs."
  ],
  [
    "Whenever this algorithm encodes strings, it MUST use UTF-8 encoding.",
    "Whenever this algorithm encodes strings, it MUST use UTF-8 encoding."
  ],
  [
    "If one or more of the proof.type, proof.verificationMethod, and proof.proofPurpose values is not set, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
    "If one or more of proof.type, proof.verificationMethod, and proof.proofPurpose does not exist, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR"
  ],
  [
    "If a proof with id equal to previousProof does not exist in allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
    "If a proof with id equal to previousProof does not exist in allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR."
  ],
  [
    "If either securedDocument is not a map or securedDocument.proof is not a map, an error MUST be raised and SHOULD convey an error type of PARSING_ERROR.",
    "If either securedDocument is not a map or securedDocument.proof is not a map, an error MUST be raised and SHOULD convey an error type of PARSING_ERROR."
  ],
  [
    "If expectedProofPurpose was given, and it does not match proof.proofPurpose, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
    "If expectedProofPurpose was given, and it does not match proof.proofPurpose, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR."
  ],
  [
    "If any element of previousProof list has an id attribute value that does not match the id attribute value of any element of allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
    "If any element of previousProof list has an id attribute that does not match the id attribute of any element of allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR."
  ],
  [
    "When expressing a data integrity proof on an object, a proof property MUST be used",
    "When expressing a data integrity proof on an object, a proof property MUST be used."
  ],
  [
    "The reason the proof was created MUST be specified as a string that maps to a URL [URL]",
    "The reason the proof was created ('proof.proofPurpose') MUST be specified as a string that maps to a URL."
  ],
  [
    "If specified, its value MUST be a string.",
    "If specified (proof.cryptosuite), its value MUST be a string."
  ],
  [
    "When deserializing to RDF, implementations MUST ensure that the base URL is set to null.",
    "When deserializing to RDF, implementations MUST ensure that the base URL is set to null."
  ],
  [
    "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite",
    "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite."
  ],
  [
    "Cryptographic suite designers MUST use mandatory proof value properties defined in Section 2.1 Proofs, and MAY define other properties specific to their cryptographic suite.",
    "Cryptographic suite designers MUST use mandatory proof value properties defined in Section 2.1 Proofs, and MAY define other properties specific to their cryptographic suite."
  ],
  [
    "If the algorithm produces an error, the error MUST be propagated and SHOULD convey the error type.",
    "If the algorithm produces an error, the error MUST be propagated and SHOULD convey the error type."
  ]
]
```
#### Unmatched Test Suite Statements
```json
[
  "('proof.id') An optional identifier for the proof, which MUST be a URL.",
  "A verification method is the means and information needed to verify the proof. If included, the value MUST be a string that maps to a [URL].",
  "('proof.proofValue') A string value that expresses base-encoded binary data necessary to verify the digital proof using the verificationMethod specified. The value MUST use a header and encoding as described in Section 2.4 Multibase of the Controller Documents 1.0 specification to express the binary data.",
  "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite. If the processing environment supports subtypes of string, the type of the cryptosuite value MUST be the https://w3id.org/security#cryptosuiteString subtype of string.",
  "The type property MUST contain the string DataIntegrityProof.",
  "The proofValue property MUST be used, as specified in 2.1 Proofs.",
  "('proof.proofValue') A string value that contains the base-encoded binary data necessary to verify the digital proof using the verificationMethod specified. The contents of the value MUST be expressed with a header and encoding as described in Section 2.4 Multibase of the Controller Documents 1.0 specification.",
  "Implementations that use JSON-LD processing, such as RDF Dataset Canonicalization [RDF-CANON], MUST throw an error, which SHOULD be DATA_LOSS_DETECTION_ERROR, when data is dropped by a JSON-LD processor, such as when an undefined term is detected in an input document.",
  "The value of the cryptosuite property MUST be a string that identifies the cryptographic suite. If the processing environment supports subtypes of string, the type of the cryptosuite value MUST be the https://w3id.org/security#cryptosuiteString subtype of string.",
  "An OPTIONAL string value (proof.previousProof) or unordered list of string values. Each value identifies another data integrity proof that MUST verify before the current proof is processed.",
  "If an unordered list (proof), all referenced proofs in the array MUST verify.",
  "The type property MUST be DataIntegrityProof.",
  "The cryptosuite property of the proof MUST be eddsa-rdfc-2022 or eddsa-jcs-2022.",
  "The proofValue property of the proof MUST be a detached EdDSA signature produced according to [RFC8032], encoded using the base-58-btc header and alphabet as described in the Multibase section of Controller Documents 1.0.",
  "The publicKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed.",
  "The secretKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed. (secretKeyMultibase)",
  "The type property MUST be DataIntegrityProof.",
  "The cryptosuite property of the proof MUST be eddsa-rdfc-2022 or eddsa-jcs-2022.",
  "The proofValue property of the proof MUST be a detached EdDSA signature produced according to [RFC8032], encoded using the base-58-btc header and alphabet as described in the Multibase section of Controller Documents 1.0.",
  "The publicKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed.",
  "The secretKeyMultibase value of the verification method MUST start with the base-58-btc prefix (z), as defined in the Multibase section of Controller Documents 1.0.",
  "Any other encoding MUST NOT be allowed. (secretKeyMultibase)",
  "The transformation options MUST contain a type identifier for the cryptographic suite (type) and a cryptosuite identifier (cryptosuite).",
  "If options.type is not set to the string DataIntegrityProof and options.cryptosuite is not set to the string eddsa-jcs-2022, an error MUST be raised that SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MUST contain a cryptosuite identifier (cryptosuite).",
  "If proofConfig.type is not set to DataIntegrityProof or proofConfig.cryptosuite is not set to eddsa-jcs-2022, an error MUST be raised that SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If proofConfig.created is set to a value that is not a valid [XMLSCHEMA11-2] datetime, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MAY contain a cryptosuite identifier (cryptosuite).",
  "The transformation options MUST contain a type identifier for the cryptographic suite (type) and a cryptosuite identifier  (cryptosuite).",
  "Whenever this algorithm encodes strings, it MUST use UTF-8 encoding.",
  "If options.type is not set to the string DataIntegrityProof and options.cryptosuite is not set to the string eddsa-rdfc-2022, an error MUST be raised that SHOULD convey an error type of PROOF_TRANSFORMATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MUST contain a cryptosuite identifier (cryptosuite).",
  "If proofConfig.type is not set to DataIntegrityProof and/or proofConfig.cryptosuite is not set to eddsa-rdfc-2022, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If proofConfig.created is present and set to a value that is not a valid [XMLSCHEMA11-2] datetime, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "The proof options MUST contain a type identifier for the cryptographic suite (type) and MAY contain a cryptosuite identifier (cryptosuite).",
  "An OPTIONAL string value (proof.previousProof) or unordered list of string values. Each value identifies another data integrity proof that MUST verify before the current proof is processed."
]
```
#### Unmatched Specifications Statements
```json
[
  "The key words MAY, MUST, MUST NOT, OPTIONAL, and SHOULD in this document are to be interpreted as described in BCP 14 [RFC2119] [RFC8174] when, and only when, they appear in all capitals, as shown here.",
  "An optional identifier for the proof, which MUST be a URL [URL], such as a UUID as a URN (urn:uuid:6a1676b8-b51f-11ed-937b-d76685a20ff5)",
  "If included, the value MUST be a string that maps to a [URL]",
  "The date and time the proof was created is OPTIONAL and, if included, MUST be specified as an [XMLSCHEMA11-2] dateTimeStamp string, either in Universal Coordinated Time (UTC), denoted by a Z at the end of the value, or with a time zone offset relative to UTC",
  "If present, it MUST be an [XMLSCHEMA11-2] dateTimeStamp string, either in Universal Coordinated Time (UTC), denoted by a Z at the end of the value, or with a time zone offset relative to UTC",
  "If specified, the associated value MUST be either a string, or an unordered set of strings",
  "The value MUST use a header and encoding as described in Section 2.4 Multibase of the Controller Documents 1.0 specification to express the binary data",
  "If present, it MUST be a string value or an unordered list of string values",
  "If present, the digestMultibase value MUST be a single string value, or an list of string values, each of which is a Multibase-encoded Multihash value.",
  "Implementations that perform JSON-LD processing MUST treat the following JSON-LD context URLs as already resolved, where the resolved document matches the corresponding hash values below:",
  "Implementations that perform RDF processing MUST treat the JSON-LD serialization of the vocabulary URL as already dereferenced, where the dereferenced document matches the corresponding hash value below.",
  "Applications MUST use the algorithm in Section 4.6 Context Validation, or one that achieves equivalent protections, to validate contexts in a conforming secured document",
  "Context validation MUST be run after running the applicable algorithm in either Section 4.4 Verify Proof or Section 4.5 Verify Proof Sets and Chains.",
  "However, if an @context declaration is not included, extensions (such as the addition of new properties) related to this specification or corresponding cryptosuites MUST NOT be made.",
  "The specification MUST be published as a human-readable document at a URL.",
  "The specification MUST identify a cryptographic suite type and any parameters that can be used with the suite.",
  "The specification MUST detail the transformation algorithms (if any), parameters, and other necessary details, used to modify input data into the data to be protected.",
  "The specification MUST detail the hashing algorithms parameters, and other necessary details used to perform cryptographic hashing to the data to be protected.",
  "The specification MUST detail the proof serialization algorithms, parameters, and other necessary details used to perform cryptographic protection of the data.",
  "The specification MUST detail the proof verification algorithms, parameters, and other necessary details used to perform cryptographic verification of the data.",
  "The specification MUST define a data integrity cryptographic suite instantiation algorithm that accepts a set of options (map options) and returns a cryptosuite instance (struct cryptosuite)",
  "The specification MUST detail any known resource starvation attack that can occur in an algorithm and provide testable mitigations against each attack.",
  "The specification MUST contain a Security Considerations section detailing security considerations specific to the cryptographic suite.",
  "The specification MUST contain a Privacy Considerations section detailing privacy considerations specific to the cryptographic suite.",
  "The JSON-LD context associated with the cryptographic suite MUST have its terms protected from unsafe redefinition, by use of the @protected keyword.",
  "If the processing environment supports string subtypes, the subtype of the cryptosuite value MUST be the https://w3id.org/security#cryptosuiteString subtype.",
  "If options has a non-null domain item, it MUST be equal to proof.domain or an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If options has a non-null challenge item, it MUST be equal to proof.challenge or an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "If any element of previousProof list has an id attribute that does not match the id attribute of any element of allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_GENERATION_ERROR.",
  "When a step says 'an error MUST be raised', it means that a verification result MUST be returned with a verified value of false and a non-empty errors list.",
  "If one or more of proof.type, proof.verificationMethod, and proof.proofPurpose does not exist, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR.",
  "If domain was given, and it does not contain the same strings as proof.domain (treating a single string as a set containing just that string), an error MUST be raised and SHOULD convey an error type of INVALID_DOMAIN_ERROR.",
  "If challenge was given, and it does not match proof.challenge, an error MUST be raised and SHOULD convey an error type of INVALID_CHALLENGE_ERROR.",
  "If a proof with id value equal to the value of previousProof does not exist in allProofs, an error MUST be raised and SHOULD convey an error type of PROOF_VERIFICATION_ERROR",
  "The type value of the error object MUST be a URL that starts with the value https://w3id.org/security# and ends with the value in the section listed below.",
  "The code value MUST be the integer code described in the table below (in parentheses, beside the type name)."
]
```