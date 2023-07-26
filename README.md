# INDIGO's graffiti thesaurus - structure documentation
The INDIGO graffiti thesaurus is a controlled vocabulary that organizes and classifies terms and concepts related to graffiti, street art, and human-made markings. The thesaurus is based on the SKOS data model and is built using the open-source software Skosmos. It is structured in a hierarchical fashion, with facets, hierarchy names, guide terms, and concepts used to organize and classify the vocabulary. The thesaurus is derived from the Getty AAT, but also includes concepts and labels specific to the graffiti and street art domain. The thesaurus also provides an easy way to link external concepts, like wikidata and Getty AAT, to the main concepts of the thesaurus. The thesaurus can be browsed and searched with a web-based interface, and can be accessed via a REST-API for linked data integration via the Vocabs service.


## The Getty AAT
The Getty Art & Architecture Thesaurus (AAT) is a structured vocabulary developed by the J. Paul Getty Trust, which provides standardized terms for describing and indexing visual arts, architecture, and related materials. It is used by museums, libraries, archives, and other cultural institutions to index and catalog art-related information. It can also improve access to information about art, architecture, and other material culture. The AAT is part of a suite of Getty Vocabularies, including the Getty Thesaurus of Geographic Names, the Union List of Artist Names, the Cultural Objects Name Authority, and the Iconography Authority. These resources can be used for cataloging, linking, retrieval, and research and are available in various formats, such as Linked Open Data, XML, and relational tables, as well as through online search tools and APIs [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?Im8xZA). 


### Facets
In the Getty Art & Architecture Thesaurus (AAT), a facet is a category or classification scheme used to organize and navigate the thesaurus, grouping similar concepts together for more efficient and intuitive searching [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?eqqf41).


### Hierarchy Names
In the Getty Art & Architecture Thesaurus (AAT), the hierarchy names are used to structure and organize the concepts and terms within the thesaurus by indicating the broader or narrower context of a given concept, creating a hierarchical tree branching from the root "Top of the AAT Hierarchies" [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?2HrRAE).


### Guide Terms
In the Getty Art & Architecture Thesaurus (AAT), Guide terms are a feature that helps users navigate the thesaurus by providing a list of recommended terms to explore related concepts and narrowing down their search.


### Concepts
In the Getty Art & Architecture Thesaurus (AAT), a concept is a central idea or theme represented by one or more terms linked to other concepts by relationships such as hierarchical, equivalent, or associative relationships. Each concept is identified by a unique numeric ID [(About the AAT (Getty Research Institute). 2023)](https://www.zotero.org/google-docs/?GZQP03).


## SKOS and Skosmos
SKOS (Simple Knowledge Organization System) is a standard for representing thesauri, classification schemes, taxonomies, and other types of controlled vocabulary using RDF (Resource Description Framework) format. It provides a set of concepts and relationships that can be used to describe hierarchical and non-hierarchical structures of knowledge in a machine-readable way. This allows for interoperability between different vocabularies and enables the reuse of existing vocabularies in different applications. One can use SKOS for creating, managing, and publishing vocabularies, as well as for integrating different vocabularies into a single system [(Alistair Miles et al. 2009)](https://www.zotero.org/google-docs/?MI19wB).


### Skosmos
Skosmos is a web-based tool for browsing and editing SKOS vocabularies. It provides a user-friendly interface for browsing and searching the concepts in a vocabulary, as well as editing and managing the vocabulary's metadata. Skosmos also includes a number of built-in features such as concept suggestions, language support, and visualization tools. It can be used to create and publish vocabularies on the web, and also allows for easy integration with other systems and applications. With Skosmos, users can access, publish and share their vocabularies with others [(Suominen et al.)](https://www.zotero.org/google-docs/?AV1i2t).


#### Collection
In Skosmos, a "collection" is a grouping of concepts within a controlled vocabulary. It allows for organizing concepts in a logical way, such as grouping concepts by theme or subject matter. Collections can be defined by the vocabulary creator, and they can be hierarchical, meaning that a collection can contain other collections or concepts.
Collections can be used to group together related concepts, making it easier to browse and search for specific information within the vocabulary. For example, in a thesaurus about art, a collection could be created for "Painting Techniques" and include concepts such as "Oil Painting," "Acrylic Painting," and "Watercolor Painting." Additionally, collections can be used to group together concepts that are used together in a specific context or application, such as a collection of concepts related to a specific project or dataset.
In Skosmos, collections can be created and managed through the web-based Vocabs editor tool, which allows for adding, editing, and deleting collections, as well as adding and removing concepts from collections. The Skosmos API also allows for managing collections programmatically.
In summary, collections in Skosmos are a useful way to organize concepts in a controlled vocabulary by grouping them in a logical way, making it easier to browse and search for specific information within the vocabulary.


### Vocabs
The Vocabs service provides a suite of tools and resources for the management of controlled vocabularies, such as gazetteers, thesauri and taxonomies, made available by the Austrian Centre for Digital Humanities (ACDH-CH). The service is built on Skosmos, an open-source software, and utilizes the SKOS data model which is a standard for representing controlled vocabularies in RDF (Resource Description Framework) format. The Vocabs repository, a web-based tool, allows for browsing and searching of vocabularies, with the ability to display structured concepts and visualize concept hierarchies, it also allows for access to the vocabularies via a REST-API, which enables linked data. The Vocabs repository is not only used for internal purposes by ACDH-CH but also for partners of the national CLARIAH-AT consortium, for the Thesaurus Maintenance working group in DARIAH-EU, and for WP6 - Services and tools in PARTHENOS [(Vocabs services. 2023)](https://www.zotero.org/google-docs/?eRwDvE).


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

