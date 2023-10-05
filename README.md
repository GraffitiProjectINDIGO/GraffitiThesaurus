# Structure of INDIGO's graffiti thesaurus
The INDIGO graffiti thesaurus is a specialised tool that categorises and organises concepts related to graffiti using a system known as a controlled vocabulary. In the context of a thesaurus, a concept refers to an idea or mental image that represents a particular entity or topic. A controlled vocabulary is a set of standardised concepts that ensures consistency when describing and categorising information. The thesaurus is based on the [SKOS](https://www.w3.org/2009/08/skos-reference/skos.html) (Simple Knowledge Organization System) data model, a widely accepted standard for sharing and linking knowledge organisation systems on the web. It allows for the easy sharing and reuse of knowledge across different applications and communities, making our thesaurus more accessible and interoperable. This means that the concepts in the graffiti thesaurus can be easily linked with other resources like [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) or the [Getty Art & Architecture Thesaurus (AAT)](https://www.getty.edu/research/tools/vocabularies/aat), enhancing the richness and depth of the information provided.

The thesaurus is available [here](https://vocabs.acdh.oeaw.ac.at/indigo_browse/). It is hosted by the [Vocabs](https://vocabs.acdh.oeaw.ac.at) service of the Austrian Centre for Digital Humanities and Cultural Heritage ([ACDH-CH](https://www.oeaw.ac.at/acdh/acdh-ch-home)), a research institution dedicated to the application of digital methods and tools in the field of humanities and cultural heritage. Vocabs is a platform that utilises [Skosmos](https://skosmos.org/), an open-source software designed for publishing and using vocabularies. The structure of the graffiti thesaurus is taken from the AAT, using facets, hierarchy names, and guide terms to organise the content. Each concept within the thesaurus can be accessed and searched for by directing a web browser to its unique Uniform Resource Identifier (URI), provided by the Vocabs service. This URI acts as a specific web address for each concept, allowing for direct access and retrieval of information.

For integration into other systems, the thesaurus can be accessed via a REST (Representational State Transfer) API (Application Programming Interface) through the Vocabs service. REST APIs are standard methods for interacting with data over the internet, using HTTP (Hypertext Transfer Protocol) methods. The Vocabs service REST API allows operations such as searching for concepts and retrieving specific concept information. Detailed instructions for using this API are available in the [Swagger documentation](https://vocabs-api.acdh.oeaw.ac.at).


## The Art & Architecture Thesaurus
[Getty Art & Architecture Thesaurus (AAT)](https://www.getty.edu/research/tools/vocabularies/aat) is a structured vocabulary developed by the J. Paul Getty Trust. It provides standardised terms for describing and indexing visual arts, architecture, and related materials. Museums, libraries, archives, and other cultural institutions use the AAT, which is part of a suite of Getty Vocabularies including the [Getty Thesaurus of Geographic Names](https://www.getty.edu/research/tools/vocabularies/tgn/), the [Union List of Artist Names](https://www.getty.edu/research/tools/vocabularies/ulan/), the [Cultural Objects Name Authority](https://www.getty.edu/research/tools/vocabularies/cona/), and the [Iconography Authority](https://www.getty.edu/research/tools/vocabularies/cona/index.html). These resources can be used for cataloguing, linking, retrieving, or researching data. All controlled vocabularies are available in various formats such as JSON (a lightweight data-interchange format), XML (a markup language that encodes documents in a machine-readable format), and [Turtle](https://www.w3.org/TR/turtle))  (a syntax for expressing data in the Resource Description Framework), as well as through online search tools and APIs [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?Im8xZA). 


### Facets
In the AAT, a facet is a category or classification scheme used to organise and navigate the thesaurus, grouping similar concepts for more efficient and intuitive searching [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?eqqf41). An example of this in the AAT is the "Styles and Periods Facet” (http://vocab.getty.edu/page/aat/300264088), which groups together various art and architectural styles and periods such as "Baroque", "Gothic", and "Wildstyle (graffiti)".


### Hierarchy Names
Hierarchy names in the AAT are used to structure and organise the concepts within the thesaurus. They indicate the broader or narrower context of a given concept, creating a hierarchical tree branching from the root "Top of the AAT Hierarchies" [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?2HrRAE). However, in the INDIGO graffiti thesaurus, the top term "Top of the AAT Hierarchies" is not used, instead, the hierarchy might start with the facets. Overall this hierarchical structure allows users to navigate from broader to more specific terms, helping them to locate the most relevant information. For instance, under the hierarchy name “Materials (hierarchy name)” (http://vocab.getty.edu/page/aat/300010357), which encompasses a broad range of substances, from natural and synthetic raw materials to material products.


### Guide Terms
Guide terms in the AAT are a feature that helps users navigate the thesaurus. They provide a list of recommended terms to explore related concepts and assist in narrowing down a search. As an example, under the guide term "< physical activities by general context >" (http://vocab.getty.edu/page/aat/300239443), which is located under the "Activities Facet", then "Physical and Mental Activities" hierarchy, users are directed to explore related concepts such as "beating (general physical activity)", "closing (activity)", "mistreating", "opening (activity)", and "working". These guide terms serve as a roadmap, helping users to navigate the complex network of concepts within the thesaurus.


### Concepts
In the AAT, a concept is a central idea or theme represented by one or more terms. Concepts are linked to other concepts by hierarchical, equivalent, or associative relationships, creating a network of related ideas. Each concept is identified by a unique numeric identifier (ID) [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?GZQP03). For example, in the Getty AAT, the concept of "Baroque" (http://vocab.getty.edu/page/aat/300021147) is represented by a unique ID (300021147), and is linked to related concepts like "Renaissance" or "Roccoco". This interconnected web of concepts allows users to explore a topic from multiple angles, providing a richer and more comprehensive understanding of the subject matter.


## SKOS and Skosmos
### SKOS
[SKOS](https://www.w3.org/2009/08/skos-reference/skos.html), or Simple Knowledge Organization System, is a recommendation by the World Wide Web Consortium ([W3C](https://www.w3.org/TR/skos-reference)) for representing various types of controlled vocabulary, such as thesauri, classification schemes, taxonomies.  It uses the Resource Description Framework ([RDF](https://www.w3.org/RDF)) format, providing a set of concepts and relationships to describe both hierarchical and non-hierarchical knowledge structures in a machine-readable way. This facilitates interoperability between different vocabularies and enables the reuse of existing vocabularies in different applications. SKOS is used for creating, managing, and publishing vocabularies, as well as for integrating different vocabularies into a single system [(Alistair Miles et al. 2009)](https://www.zotero.org/google-docs/?MI19wB).


### Skosmos
[Skosmos](https://skosmos.org) is a web-based tool that complements SKOS by providing a platform for browsing and searching the concepts in a vocabulary, as well as managing the vocabulary's metadata. It includes built-in features such as concept suggestions, language support, and visualisation tools. Skosmos is used to publish vocabularies on the web, allowing for easy integration with other systems and applications. It enables users to access, publish and share their vocabularies with others [(Suominen et al.)](https://www.zotero.org/google-docs/?AV1i2t).


### Collection
Within SKOS, the vocabulary creator can define a [collection](https://www.w3.org/TR/skos-reference/#collections), which is a grouping of concepts within a controlled vocabulary. Collections facilitate the logical, even nested, organisation of concepts by theme or subject matter, aiding in browsing and searching for specific information. For example, in a thesaurus about art, a collection could be created for "Painting Techniques" and include concepts such as "Oil Painting", "Acrylic Painting", and "Watercolour Painting." Additionally, collections can also group concepts that often used together in a specific context or application, like all concepts used in a project or dataset. These collections can be created and managed through the Vocabs editor tool (see the next paragraph). The Skosmos REST API, and its specific implementation in Vocabs, allows for programmatic access to collections.


### Vocabs
The [Vocabs](https://vocabs.dariah.eu/en/) , provided by the Austrian Centre for Digital Humanities and Cultural Heritage ([ACDH-CH](https://www.oeaw.ac.at/acdh/acdh-ch-home)), offers tools and resources for managing controlled vocabularies. Built on Skosmos and utilising the SKOS data model (see the previous paragraphs), Vocabs includes a web-based browser for exploring and searching vocabularies or displaying the structured concepts and their hierarchies. Vocabularies are also accessible over a REST API, enhancing the reuse of these data in different contexts [(Vocabs services. 2023)](https://www.zotero.org/google-docs/?eRwDvE).


## The INDIGO graffiti thesaurus

### TSV Files
TSV stands for Tab-Separated Values. It is a simple file format used to store data in a tabular structure, akin to a CSV (Comma-Separated Values) file. Each line in a TSV file represents a row in the table, and each field in the row is separated by a tab character. This format is widely utilised for its simplicity and compatibility with numerous data processing tools and applications. For instance, a TSV file can be effortlessly opened and edited in a spreadsheet programme such as Microsoft Excel or Google Sheets. It can also be processed using programming languages like Python or R, which provide built-in functions for reading and writing TSV files.

### JSON Files
JSON stands for JavaScript Object Notation. It is a lightweight data-interchange format that is straightforward for humans to read and write and simple for machines to parse and generate. JSON is a text format that is entirely language-independent but utilises conventions that are familiar to programmers of the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others. In a JSON file, data is represented in a structured manner using two types of structures:
1. A collection of key/value pairs. In various languages, this is realised as an object, record, struct, dictionary, hash table, keyed list, or associative array.
2. An ordered list of values. In most languages, this is realised as an array, vector, list, or sequence.
These are universal data structures that are supported in some form by nearly all modern programming languages. This makes JSON a highly useful format for data interchange between different programming languages. For instance, a JSON file can be easily processed using JavaScript, Python, or many other programming languages, which provide built-in functions for parsing JSON data and converting it into native data structures. It can also be used in web APIs to send and receive data between a client and a server.

### The structure

The INDIGO graffiti thesaurus is structured as a set of concepts, each represented as an object in a JSON file. Each concept includes several data fields that provide information about the concept and its relationships with other concepts.

In the thesaurus, the "Listing terms separator" is used to separate different labels of a concept or multiple external concepts linked to a concept. The separator used is "\$\$". For example, "antistyle \$\$ anti style (graffiti)". The same also works for multiple external concepts, for example, "http://vocab.getty.edu/page/aat/300015613 \$\$ http://vocab.getty.edu/page/aat/300410270".

In the following sections, we will describe each data field in detail using the example of the concept _"tags (graffiti)"_.

#### Unique identifier

_**Example:** "tagsGraffiti"_

The "Unique identifier" is a string that serves as a unique reference to each concept in the thesaurus. It ensures that each concept can be referenced, retrieved, and manipulated individually, without confusion or error. The unique identifier is typically a combination of alphanumeric characters, and it may include capital letters for readability. In the context of the INDIGO project, the unique identifier is not only unique but also designed to be easily readable and interpretable. It is incorporated into the Uniform Resource Identifier (URI) for each concept, enabling users to easily locate and understand the concept based on its unique identifier. This approach enhances the usability and accessibility of the thesaurus, making it easier for users to navigate and interact with the data.

#### Type

_**Example:** "concept"_

The "Type" field specifies the type of entity being described. This classification is based on the standards set by the Art & Architecture Thesaurus (AAT) or the Simple Knowledge Organization System (SKOS). The type can be a facet, hierarchy name, guide term, concept, or collection, as defined by the AAT or SKOS. In the context of the INDIGO project, the "Type" field serves multiple purposes. Firstly, it helps to organise and classify the concepts within the thesaurus, providing a clear and consistent structure. This makes it easier for users to navigate the thesaurus and understand the relationships between different concepts.

Secondly, the "Type" field helps to track the origin and rationale behind each concept. By specifying whether a concept is a facet, hierarchy name, guide term, concept, or collection, the "Type" field provides insight into the thought process and decision-making that went into the creation of the thesaurus. This can be useful for users who want to understand the underlying principles and methodologies of the thesaurus. Lastly, by adhering to the standards set by the AAT and SKOS, the "Type" field ensures that the thesaurus is interoperable with other resources that use the same standards. This enhances the usability and versatility of the thesaurus, allowing it to be integrated with other systems and utilised in a variety of contexts.

#### skos:prefLabel @en

_**Example:** "tags (graffiti)"_

The "skos:prefLabel @en" field provides the preferred label for the concept in English. This is the primary label that represents the concept within the thesaurus. It is used as the main identifier for the concept in search results and other interfaces where the concept is presented. The preferred label is carefully chosen to accurately and succinctly represent the essence of the concept, making it easier for users to understand and interact with the data.

#### skos:broader

_**Example:** "writingGraffiti"_

The "skos:broader" field specifies the broader concept under which the current concept falls. This establishes a hierarchical relationship between concepts, allowing users to navigate from more specific to more general concepts.

In the context of the INDIGO project, the "skos:broader" field is used to manually define the broader concept for each concept in the thesaurus. Once the broader concept is defined, the corresponding "skos:narrower" relationship is automatically generated. This approach ensures consistency and accuracy in the hierarchical structure of the thesaurus, preventing errors such as missing concepts or incorrectly specified relationships.

#### rdf:type (skos:)

_**Example:** "Concept"_

The "rdf:type (skos:)" field specifies the type of the entity according to the Simple Knowledge Organization System (SKOS) data model. In the context of the INDIGO project, the type can be either a "Concept" or a "Collection".

This classification helps to organise and classify the entities within the thesaurus, providing a clear and consistent structure. By specifying the type of each entity, users can easily understand the nature of the entity and its role within the thesaurus. This enhances the usability of the thesaurus and facilitates more effective navigation and interaction with the data.

#### skos:member

_**Example:** "graffitoType"_

The "skos:member" field indicates whether the concept or collection being described is a member of a specific collection. This field is used to group related concepts within the thesaurus, enhancing the organisation and navigability of the data.

In the context of the INDIGO project, the "skos:member" field is used to create logical groupings of related concepts. These groupings can help users explore the thesaurus more effectively, as they can easily find and examine sets of related concepts. This can be particularly useful for users who are interested in a specific theme or topic, as they can easily locate all the concepts related to that theme or topic.

#### skos:altLabel @en

_**Example:** "tag (graffiti) \$$ tag \$$ tags"_

The "skos:altLabel @en" field provides alternative labels for the concept in English. These are additional terms that can be used to represent the concept, and they are often synonyms or variant spellings of the preferred label. Alternative labels are particularly useful in search operations. If a user searches for a term that is not the preferred label for a concept, but is listed as an alternative label, the search operation will still return the correct concept. This increases the likelihood that users will find the information they are looking for, even if they use different terminology.

In the context of the INDIGO project, the "skos:altLabel @en" field is used to ensure that the thesaurus is accessible and user-friendly. By providing a range of terms for each concept, the thesaurus can accommodate a variety of user needs and preferences, making it a more versatile and useful tool.

#### skos:editorialNote @en

_**Example:** ""Tags (graffiti)" refers to a specific type of graffiti writing. A tag is essentially the signature or moniker of a graffitist, often stylised in a unique and distinctive way. It is the simplest and most fundamental form of graffiti, and it is typically the first type of graffiti that a graffitist learns to create. Tags are usually created quickly and can be found in a variety of locations throughout urban environments. They are often used by graffitists to mark territory, gain recognition, or participate in the broader graffiti community. While tags may appear simple or even crude to the untrained eye, they can be rich in meaning and style. The design of a tag can convey a great deal of information about the graffitist, including their skill level, their influences, and their place within the graffiti community."_

The "skos:editorialNote @en" field provides an editorial note in English. In the current state of the INDIGO project, this field is used to explain what the concept means to the creators of the thesaurus. It provides an understanding of the concept as it is currently defined, serving as a guideline for users on how to interpret and use the concept.

However, it's important to note that the use of the "skos:editorialNote @en" field in this way is a temporary solution. In future updates to the INDIGO project, the actual description of the concept will be provided in the "skos:definition @en" field. At that point, the "skos:editorialNote @en" field will likely be used for different purposes, such as providing additional context or clarification about the concept.

#### skos:note @en (getty)

_**Example:** ""Stylized forms of graffiti using names or initials as markers. These are considered the most basic form of graffiti art." (Art & Architecture Thesaurus Full Record Display (Getty Research). ‘Tags (Documents)’)"_

The "skos:note @en (getty)" field provides a note in English about the concept, as provided by the Getty Art & Architecture Thesaurus (AAT). This note is directly quoted from the Getty AAT and is included in the INDIGO thesaurus to provide additional context and understanding about the concept.

The note is enclosed in quotation marks to indicate that it is a direct quote, and a citation is included to credit the source of the information. The full bibliographic information for the citation is then included in the "dc:source @en" field. This approach ensures that the source of the information is properly credited and that users can refer to the original source if they wish to explore the concept in more detail.

#### external concept (getty)

_**Example:** "http://vocab.getty.edu/page/aat/300410284"_

The "external concept (getty)" field provides a link to a related concept in the Getty Art & Architecture Thesaurus (AAT). This field is used to connect the concepts in the INDIGO thesaurus with related concepts in the Getty AAT, enhancing the richness and depth of the information provided.

By linking to external concepts, the INDIGO thesaurus can provide users with a broader context for each concept and enable them to explore related ideas in more detail. This can be particularly useful for users who are interested in a specific theme or topic, as they can easily locate additional information and resources related to that theme or topic.

#### type of match (getty) (skos:exactMatch, skos:closeMatch, skos:broadMatch, skos:narrowMatch, skos:relatedMatch)

_**Example:** "exactMatch"_

The "type of match (getty)" field specifies the type of match between the concept in the INDIGO thesaurus and an external concept from the Getty Art & Architecture Thesaurus (AAT). This field is used to indicate the degree of similarity or relatedness between the two concepts.

The different types of matches are defined as follows:

- skos:exactMatch: The concept in the INDIGO thesaurus is semantically equivalent to the external concept from the Getty AAT. They can be used interchangeably in the same context.
- skos:closeMatch: The concept in the INDIGO thesaurus is very similar to the external concept from the Getty AAT, but they may not be used interchangeably in all contexts due to minor differences in meaning.
- skos:broadMatch: The external concept from the Getty AAT is more general than the concept in the INDIGO thesaurus. The INDIGO concept is a type of the Getty concept.
- skos:narrowMatch: The external concept from the Getty AAT is more specific than the concept in the INDIGO thesaurus. The Getty concept is a subtype of the INDIGO concept.
- skos:relatedMatch: The concept in the INDIGO thesaurus is related to the external concept from the Getty AAT, but they are not equivalent or hierarchical. They share a semantic relationship.

By specifying the type of match, the INDIGO thesaurus provides users with a clearer understanding of the relationship between the concepts in the thesaurus and the related concepts in the Getty AAT.

#### external concept (wikidata)

_**Example:** "https://www.wikidata.org/wiki/Q17514"_

The "external concept (wikidata)" field provides a link to a related concept in Wikidata. This field is used to connect the concepts in the INDIGO thesaurus with related concepts in Wikidata, enhancing the richness and depth of the information provided.

By linking to external concepts, the INDIGO thesaurus can provide users with a broader context for each concept and enable them to explore related ideas in more detail. This can be particularly useful for users who are interested in a specific theme or topic, as they can easily locate additional information and resources related to that theme or topic.

#### type of match (wikidata) (skos:exactMatch, skos:closeMatch, skos:broadMatch, skos:narrowMatch, skos:relatedMatch)

_**Example:** "relatedMatch"_

The "type of match (wikidata)" field specifies the type of match between the concept in the INDIGO thesaurus and an external concept from Wikidata. This field is used to indicate the degree of similarity or relatedness between the two concepts.

The different types of matches are defined as follows:

- skos:exactMatch: The concept in the INDIGO thesaurus is semantically equivalent to the external concept from Wikidata. They can be used interchangeably in the same context.
- skos:closeMatch: The concept in the INDIGO thesaurus is very similar to the external concept from Wikidata, but they may not be used interchangeably in all contexts due to minor differences in meaning.
- skos:broadMatch: The external concept from Wikidata is more general than the concept in the INDIGO thesaurus. The INDIGO concept is a type of the Wikidata concept.
- skos:narrowMatch: The external concept from Wikidata is more specific than the concept in the INDIGO thesaurus. The Wikidata concept is a subtype of the INDIGO concept.
- skos:relatedMatch: The concept in the INDIGO thesaurus is related to the external concept from Wikidata, but they are not equivalent or hierarchical. They share a semantic relationship.

By specifying the type of match, the INDIGO thesaurus provides users with a clearer understanding of the relationship between the concepts in the thesaurus and the related concepts in Wikidata.

#### dct:source

_**Example:** "Art & Architecture Thesaurus Full Record Display (Getty Research). ‘Tags (Documents)’, 25 January 2021. http://vocab.getty.edu/page/aat/300410284."_

The "dct:source" field provides the source of the information for the concept in the INDIGO thesaurus. This field is used to credit the original source of the information and to provide a reference for users who wish to explore the concept in more detail.

The source is typically a published work or a reputable online resource, and it is provided in a citation format that includes the title of the work, the author or organisation, the date of publication, and a URL or other identifier. This citation format allows users to easily locate and access the original source of the information.

By providing the source of the information, the INDIGO thesaurus ensures that the original creators of the information are properly credited, and it provides a level of transparency and accountability for the information provided in the thesaurus.

#### skos:example @en

_**Example:** "A graffitist might use a tag to mark their territory or to gain recognition within the graffiti community."_

The "skos:example @en" field provides an example of how the concept can be used in context, in English. This field is used to illustrate the practical application of the concept and to help users understand how it can be used in real-world situations.

The example is typically a sentence or short paragraph that includes the concept and shows how it can be used in a sentence or a specific context. This can be particularly useful for users who are unfamiliar with the concept or who are learning about the topic for the first time. By providing an example of how the concept can be used, the INDIGO thesaurus helps to make the concepts more accessible and understandable to a wide range of users.

#### skos:related

_**Example:** "charactagGraffiti"_

The "skos:related" field provides a reference to related concepts within the INDIGO thesaurus. This field is used to establish connections between different concepts, enhancing the richness and depth of the information provided.

By linking to related concepts, the INDIGO thesaurus can provide users with a broader context for each concept and enable them to explore related ideas in more detail. This can be particularly useful for users who are interested in a specific theme or topic, as they can easily locate additional information and resources related to that theme or topic.

#### AAT Facets in the INDIGO Graffiti Thesaurus

The INDIGO graffiti thesaurus utilises facets from the AAT to organise its concepts. Here's how we handle facets:

- Each facet's preferred label starts with a capital letter and ends with the tag "`<facet>`". For example, "`Activities <facet>`".
- The unique identifier for each facet follows the PascalCase convention (each word starts with a capital letter) and ends with a capital "F" to denote its facet status. For example, "`ActivitiesF`".
- The original notes from the AAT are retained for each facet to accurately describe the concept.
- The thesaurus currently encompasses six facets derived from the AAT:  
    - `Activities <facet>`
    - `Agents <facet>`
    - `Associated Concepts <facet>`
    - `Objects <facet>`
    - `Physical Attributes <facet>`
    - `Styles and Periods <facet>`


#### AAT Hierarchy Names in the INDIGO Graffiti Thesaurus

Hierarchy names in the INDIGO graffiti thesaurus serve to categorise concepts into broader groups. Here's how we handle hierarchy names:

- Each hierarchy name's preferred label starts with a capital letter and ends with the tag "`<hierarchy name>`". For example, "`Associated Concepts <hierarchy name>`".
- The unique identifier for each hierarchy name follows the PascalCase convention (each word starts with a capital letter), and ends with "HN" to denote its status as a hierarchy name. For example, "`AssociatedConceptsHN`".
- No additional information is typically added to the hierarchy names, as the AAT does not provide further details.
- The thesaurus currently encompasses several hierarchy names:  
    - `Associated Concepts <hierarchy name>`
    - `Built Environment <hierarchy name>`
    - `Components <hierarchy name>`
    - `Design Elements <hierarchy name>`
    - `Information Forms <hierarchy name>`
    - `Open Spaces and Site Elements <hierarchy name>`
    - `People <hierarchy name>`
    - `Physical and Mental Activities <hierarchy name>`
    - `Processes and Techniques <hierarchy name>`
    - `Styles and Periods <hierarchy name>`
    - `Visual and Verbal Communication <hierarchy name>`


#### AAT Guide Terms in the INDIGO Graffiti Thesaurus

Guide terms in the INDIGO graffiti thesaurus are utilised to organise and classify concepts. These specific terms or phrases guide users to related concepts. Here's how we handle guide terms:

- Each guide term's preferred label is written in lowercase and ends with the tag "`<guide term>`". For example, "`public and interactive activities <guide term>`".
- The unique identifier for each guide term follows the camelCase convention (first word starts with a lowercase letter, subsequent words start with a capital letter), and ends with "GT" to denote its status as a guide term. For example, "`publicAndInteractiveActivitiesGT`".
- No additional information is typically added to the guide terms, as the AAT does not provide further details.
- The thesaurus currently encompasses 21 AAT guide terms, including:  
    - `additive and joining processes and techniques <guide term>`
    - `attributes and properties by specific type <guide term>`
    - `components by specific context <guide term>`
    - `concepts in the arts and humanities <guide term>`
    - `documents by function <guide term>`
    - `open spaces by location or context <guide term>`
    - `people by occupation <guide term>`
    - `people by state or condition <guide term>`
    - `people in the arts and related occupations <guide term>`
    - `people in the humanities <guide term>`
    - `physical activities by specific context <guide term>`
    - `processes and techniques by specific type <guide term>`
    - `public and interactive activities <guide term>`
    - `script and type forms <guide term>`
    - `styles, periods, and cultures by general era <guide term>`
    - `subtractive processes and techniques <guide term>`
    - `surface covering processes and techniques <guide term>`
    - `technology and related concepts <guide term>`
    - `visual works by function <guide term>`
    - `visual works by location or context <guide term>`


#### SKOS:Concepts in the INDIGO graffiti thesaurus

Concepts are the fundamental elements of the INDIGO graffiti thesaurus. Here's how we handle concepts:

- Each concept's preferred label is written in lowercase and in plural form, unless it's a proper noun (like "Wildstyle") or an activity (like "tagging (graffiti)"), where the activity is used and no plural form is needed.
- Alternative labels are also provided for each concept, written in lowercase and separated by commas. For example, for the concept "black books (graffiti)", the alternative labels are "black book (graffiti)", "black, book", "black, books", "blackbook", "blackbooks".
- A colon is used only when the concept consists of two words, such as “black, books”.
- The thesaurus currently encompasses around 140 concepts, ranging from "@-Sign" to "writing (graffiti)".


#### SKOS:Collections in the INDIGO graffiti thesaurus

SKOS collections are utilised in the INDIGO graffiti thesaurus to group related concepts. Here's how INDIGO structures collections:

- Each collection's preferred label is written in lowercase. For example, the label for the collection of activities is "activity".
- The unique identifier for each collection is also written in lowercase. For example, the identifier for the collection of activities is "activity".
- The INDIGO graffiti thesaurus currently includes eleven collections: 
    - activity
    - community term
    - component part
    - concept idea
    - design
    - graffito class
    - graffito component
    - graffito creator
    - graffito type
    - sign and element 
    - style



## References
    [About the AAT (Getty Research Institute). 2023. Accessed January 17. https://www.getty.edu/research/tools/vocabularies/aat/about.html.](https://www.zotero.org/google-docs/?LyxcTC)
    [Alistair Miles, A. Miles & S. Bechhofer. 2009. SKOS Simple Knowledge Organization System Reference.](https://www.zotero.org/google-docs/?LyxcTC)
    [Suominen, O., H. Ylikotila, S. Pessala, M. Lappalainen, M. Frosterus, J. Tuominen, T. Baker, C. Caracciolo & A. Retterath. Publishing SKOS vocabularies with Skosmos.](https://www.zotero.org/google-docs/?LyxcTC)
    [Vocabs services. 2023. Accessed January 25. https://vocabs.acdh-dev.oeaw.ac.at/en/about#editor.](https://www.zotero.org/google-docs/?LyxcTC)

