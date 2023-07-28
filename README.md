# Structure of INDIGO's graffiti thesaurus
The INDIGO graffiti thesaurus is a specialised tool that categorises and organises concepts related to graffiti using a system known as a controlled vocabulary. In the context of a thesaurus, a concept refers to an idea or mental image that represents a particular entity or topic. A controlled vocabulary is a set of standardised concepts that ensures consistency when describing and categorising information. The thesaurus is based on the [SKOS](https://www.w3.org/2009/08/skos-reference/skos.html) (Simple Knowledge Organization System) data model, a widely accepted standard for sharing and linking knowledge organisation systems on the web. It allows for the easy sharing and reuse of knowledge across different applications and communities, making our thesaurus more accessible and interoperable. This means that the concepts in the graffiti thesaurus can be easily linked with other resources like [Wikidata](https://www.wikidata.org/wiki/Wikidata:Main_Page) or the [Getty Art & Architecture Thesaurus (AAT)](https://www.getty.edu/research/tools/vocabularies/aat), enhancing the richness and depth of the information provided.

The thesaurus is made available through the [Vocabs](https://vocabs.acdh.oeaw.ac.at) service of the Austrian Centre for Digital Humanities and Cultural Heritage ([ACDH-CH](https://www.oeaw.ac.at/acdh/acdh-ch-home)), a research institution dedicated to the application of digital methods and tools in the field of humanities and cultural heritage. Vocabs is a platform that utilises [Skosmos](https://skosmos.org/), an open-source software designed for publishing and using vocabularies. The structure of the graffiti thesaurus is taken from the AAT, using facets, hierarchy names, and guide terms to organise the content. Each concept within the thesaurus can be accessed and searched for by directing a web browser to its unique Uniform Resource Identifier (URI), provided by the Vocabs service. This URI acts as a specific web address for each concept, allowing for direct access and retrieval of information.

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
Within SKOS, the vocabulary creator can define a [collection](https://www.w3.org/TR/skos-reference/#collections), which is a grouping of concepts within a controlled vocabulary. Collections facilitate the logical, even nested, organisation of concepts by theme or subject matter, aiding in browsing and searching for specific information. For example, in a thesaurus about art, a collection could be created for "Painting Techniques" and include concepts such as "Oil Painting", "Acrylic Painting", and "Watercolour Painting." Additionally, collections can also group concepts that often used together in a specific context or application, like all concepts used in a project or dataset. These collections can be created and managed through the Vocabs editor tool (see the next paragraph). The Skosmos API, and its specific implementation in Vocabs, allows for programmatic access to collections.


### Vocabs
The [Vocabs](https://vocabs.dariah.eu/en/) , provided by the Austrian Centre for Digital Humanities and Cultural Heritage ([ACDH-CH](https://www.oeaw.ac.at/acdh/acdh-ch-home)), offers tools and resources for managing controlled vocabularies. Built on Skosmos and utilising the SKOS data model (see the previous paragraphs), Vocabs includes a web-based browser for exploring and searching vocabularies or displaying the structured concepts and their hierarchies. Vocabularies are also accessible over a REST-API, enhancing the reuse of these data in different contexts [(Vocabs services. 2023)](https://www.zotero.org/google-docs/?eRwDvE).


## The INDIGO graffiti thesaurus


### The CSV table structure
**Unique identifier —** This is a unique identifier assigned to each concept in the thesaurus, which can be used to identify and reference the concept within the thesaurus.

**Getty AAT type —** This refers to the type of term according to the Getty Art and Architecture Thesaurus (AAT). This can be used to classify and organize the concepts within the thesaurus. Here it is noted if the concept is or would be considered a facet, hierarchy name, guide term, concept or collection (SKOS) in the Getty AAT.

**skos:prefLabel @en —** This is the preferred label for the concept in English. It is the main term that will be used to represent the concept within the thesaurus and in search results.

**skos:broader —** This refers to the broader concept that the current concept falls under. It is used to establish a hierarchical structure within the thesaurus. The skos:narrower 

**rdf:type (skos:) —** This refers to the type of concept, according to the SKOS data model. It can be used to classify and organize the concepts within the thesaurus.

**skos:member —** This refers to a member of a collection. It can be used to group related concepts together within the thesaurus.

**skos:altLabel @en —** This is an alternative label for the concept in English. It can be used in search results and to provide synonyms for the concept.

**skos:editorialNote @en —** This is an editorial note in English that can be used to provide additional information or clarification about the concept.

**skos:note @en (getty) —** This is a note in English provided by Getty AAT about the concept.

**skos:note @en —** This is a note in English provided by the creator of the thesaurus about the concept.

**external concept (getty) —** This refers to an external concept from Getty AAT that is related to the current concept within the thesaurus.

**type of match (getty) (skos:exactMatch, skos:closeMatch, skos:broadMatch, skos:narrowMatch, skos:relatedMatch)—** This refers to the type of match between the current concept in the thesaurus and the external concept from Getty AAT. The different types of match indicate the degree of similarity between the two concepts.

**external concept (wikidata) —** This refers to an external concept from Wikidata that is related to the current concept within the thesaurus.

**type of match (wikidata) (skos:exactMatch, skos:closeMatch, skos:broadMatch, skos:narrowMatch, skos:relatedMatch) —** This refers to the type of match between the current concept in the thesaurus and the external concept from Wikidata. The different types of match indicate the degree of similarity between the two concepts.

**dct:source —** This refers to the source of the concept. It can be used to indicate where the information for the concept came from.

**skos:example @en —** This is an example of how the concept can be used in context, in English.

**skos:related —** This refers to related concepts within the thesaurus. It can be used to establish connections between different concepts within the thesaurus.


### The specific Getty AAT types


#### Facet
The INDIGO graffiti thesaurus uses facets to organize and classify concepts within the controlled vocabulary. A facet is a category or theme within the thesaurus that allows for grouping related concepts together.

The structure of the facets in the INDIGO graffiti thesaurus is as follows:
* The preferred label for each facet starts with a capital letter and ends with the tag "<facet>". For example, "Activities <facet>".
* In the unique identifier, each facet starts with a capital letter and every added word also starts with a capital letter. The identifier ends with a big “F” indicating that it is a facet. For example, "ActivitiesF"
* Generally, no further information is added to the facets, as the Getty AAT also does not provide any additional information.

Currently, there are 6 facets in the INDIGO thesaurus, all of which are from the Getty AAT. These facets are:
    Activities <facet>
    Agents <facet>
    Associated Concepts <facet>
    Objects <facet>
    Physical Attributes <facet>
    Styles and Periods <facet>

The structure of the facets in the INDIGO graffiti thesaurus is designed to make it easy to identify and classify the concepts within the thesaurus, and to make it easy to browse and search for specific information within the vocabulary. The use of a unique identifier also allows for easy reference and linking to the concepts within the thesaurus.


#### Hierarchy Name
In the INDIGO graffiti thesaurus, hierarchy names are used to organize and classify concepts within the controlled vocabulary by grouping them under broader categories.

The structure of the hierarchy names in the INDIGO graffiti thesaurus is as follows:
* The preferred label for each hierarchy name starts with a capital letter and ends with the tag "<hierarchy name>". For example, "Associated Concepts <hierarchy name>".
* In the unique identifier, each hierarchy name starts with a capital letter and every added word also starts with a capital letter. The identifier ends with a big “HN” indicating that it is a hierarchy name. For example, "AssociatedConceptsHN"
* Generally, no further information is added to the hierarchy names, as the Getty AAT also does not provide any additional information.

Currently, there are several hierarchy names in the INDIGO thesaurus, these are:
    Associated Concepts <hierarchy name>
    Built Environment <hierarchy name>
    Components <hierarchy name>
    Design Elements <hierarchy name>
    Information Forms <hierarchy name>
    Open Spaces and Site Elements <hierarchy name>
    People <hierarchy name>
    Physical and Mental Activities <hierarchy name>
    Processes and Techniques <hierarchy name>
    Styles and Periods <hierarchy name>
    Visual and Verbal Communication <hierarchy name>

Hierarchy names in the INDIGO graffiti thesaurus are used to organize and classify the concepts by grouping them under broader categories, making it easier to browse and search for specific information within the vocabulary. The use of a unique identifier also allows for easy reference and linking to the concepts within the thesaurus.


#### Guide Term
In the INDIGO graffiti thesaurus, guide terms are used to organize and classify concepts within the controlled vocabulary by providing a specific term or phrase that guides the user to related concepts.

The structure of the guide terms in the INDIGO graffiti thesaurus is as follows:
* The preferred label for each guide term is written in small letters and ends with the tag "<guide term>". For example, "public and interactive activities <guide term>".
* In the unique identifier, each guide term uses the camel case and ends with a “GT” indicating that it is a guide term. For example, "publicAndInteractiveActivitiesGT"
* Generally, no further information is added to the guide terms, as the Getty AAT also does not provide any additional information.

Currently, there are 21 guide terms in the INDIGO thesaurus, that are derived from the Getty AAT, such as:
    accidential surface covering processes <guide term>
    additive and joining processes and techniques <guide term>
    attributes and properties by specific type <guide term>
    components by specific context <guide term>
    concepts in the arts and humanities <guide term>
    documents by function <guide term>
    open spaces by location or context <guide term>
    people by occupation <guide term>
    people by state or condition <guide term>
    people in the arts and related occupations <guide term>
    people in the humanities <guide term>
    physical activities by specific context <guide term>
    processes and techniques by specific type <guide term>
    public and interactive activities <guide term>
    script and type forms <guide term>
    styles, periods, and cultures by general era <guide term>
    subtractive processes and techniques <guide term>
    surface covering processes and techniques <guide term>
    technology and related concepts <guide term>
    visual works by function <guide term>
    visual works by location or context <guide term>

Guide terms in the INDIGO graffiti thesaurus are used to organize and classify the concepts by providing a specific term or phrase that guides the user to related concepts, making it easier to browse and search for specific information within the vocabulary. The use of a unique identifier also allows for easy reference and linking to the concepts within the thesaurus.


#### Concept
In the INDIGO graffiti thesaurus, concepts are the core elements of the controlled vocabulary, representing the specific terms or phrases used to describe a particular idea or subject.

The structure of concepts in the INDIGO graffiti thesaurus is as follows:
* The preferred label for each concept is written in plural form and small letters, unless it is a proper name (like "writing"), a style (like "Wildstyle"), or an activity (like "tagging (graffiti)").
* Alternative labels are also included in the concepts, they are written in small letters and separated by a comma. For example, "black books (graffiti)" is the preferred label and "black book (graffiti)", "black, book", "black, books", "blackbook", "blackbooks" are alternative labels.
* So, the colon is only in use if the concept consists of two words
* There are currently 150 concepts in the INDIGO thesaurus, from "@-Sign" to "writing (graffiti)".

Concepts in the INDIGO graffiti thesaurus are the core elements of the controlled vocabulary, representing the specific terms or phrases used to describe a particular idea or subject within the graffiti, street art and human-made markings theme. Alternative labels are also included in the concepts, making it easier to find and link related concepts within the thesaurus. The use of a unique identifier also allows for easy reference and linking to the concepts within the thesaurus.


### The Skosmos types


#### Collection
In Skosmos, collections are a way to group concepts within a controlled vocabulary. A collection is a set of concepts that share a common theme or purpose.

In the INDIGO graffiti thesaurus, collections are structured as follows:
* The preferred label for each collection is written in small letters. For example, "activity".
* In the unique identifier, each collection is written in small letters as well. For example, "activity"

Currently, there are 11 collections in the INDIGO thesaurus, these are:
    activity
    community term
    component part
    concept idea
    design
    graffito class
    graffito component
    graffito creator
    graffito type
    sign and element
    style

Collections in Skosmos allow for grouping related concepts within a controlled vocabulary, making it easier to browse and search for specific information within the vocabulary. It also allows for easy reference and linking to the concepts within the thesaurus.


### Other things to note


#### Listing terms divider
The "Listing terms divider" is used to separate the different labels of a concept. The divider used is “ $$ ”. For example, “antistyle $$ anti style (graffiti)".


#### Multiple external concepts
Multiple external concepts can also be linked to a concept, these are divided by “ $$ “. For example, “http://vocab.getty.edu/page/aat/300015613 $$ http://vocab.getty.edu/page/aat/300410270”.

Currently, only one external concept linked to a concept is created so far. If more then this one external concept will be useful for the future, then the structure should be changed generally from two rows to one row with this structure: “ external concept (match type)”.


## References
    [About the AAT (Getty Research Institute). 2023. Accessed January 17. https://www.getty.edu/research/tools/vocabularies/aat/about.html.](https://www.zotero.org/google-docs/?LyxcTC)
    [Alistair Miles, A. Miles & S. Bechhofer. 2009. SKOS Simple Knowledge Organization System Reference.](https://www.zotero.org/google-docs/?LyxcTC)
    [Suominen, O., H. Ylikotila, S. Pessala, M. Lappalainen, M. Frosterus, J. Tuominen, T. Baker, C. Caracciolo & A. Retterath. Publishing SKOS vocabularies with Skosmos.](https://www.zotero.org/google-docs/?LyxcTC)
    [Vocabs services. 2023. Accessed January 25. https://vocabs.acdh-dev.oeaw.ac.at/en/about#editor.](https://www.zotero.org/google-docs/?LyxcTC)

