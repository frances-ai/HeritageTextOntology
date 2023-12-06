# HTO: The Heritage Text Ontology

The Heritage Text Ontology is designed to represent the knowledge in textual heritage. It describes a set of classes, 
properties, and restrictions that can be used to represent content and metadata of digitised historical textual collections. 
It can also capture the provenance information of digital contents and concepts. This helps to track not only the sources where 
same concepts appeared, but also how textual data was digitised and extracted. 
----

## Why building this ontology?
A large number of textual heritage has been digitised by various data providers, which provides a wealth of opportunities for
advancing research in the fields of history, culture, and linguistics. However, the heterogeneous and scale of these digital archives 
makes it difficult for researchers to search and extract meaningful information. In this case, making digitised textual collections Findable, 
Accessible, Interoperable, and Reusable (FAIR) for both humans and machines is extremely important, and building this ontology is the 
fundamental step to achieve that goal as it shares the formal representation of the knowledge in this domain.

----

## Domain and Scope

### _For what we are going to use the ontology?_

* To enable interoperability amongst systems. By using the same knowledge model,
computer systems can use this ontology and apply their own applications to it.
* To ensure reusability. The ontology is designed to be shared amongst people
and systems, and also designed in a way that facilitates later integration into other
ontologies, thus allowing its reuse.
* To facilitate knowledge acquisition. This is one of the main goals of our work.
Knowledge found in documents can be hard to extract. This ontology aims to represent 
the main concepts in documents along with their relations. Also, it intends to represent 
the temporal aspect of the knowledge. This requires linking related concepts, tracking 
provenance information from different data providers (how, when and where concepts were recorded)

### _What is the domain that the ontology will cover?_

Overall, this ontology will represent metadata (title, physical description, genre, editor, et al.) of documents, 
textual content (original text, article, abstract, concepts such as people and place) of documents, 
related provenance information (digitisation activity, software tools, editor, publisher, et al.) of the documents 
and the textual content, and relations among them. 

Note that we only focus on the literal meaning of the textual content instead of the style how text was printed or written. 
To represent all aspects of an handwritten text, please refer to [CRMtex (Model for the study
of ancient texts) ](https://cidoc-crm.org/crmtex/)

In this version, HTO is designed mainly based on the level of information extractions from this [repository](https://github.com/frances-ai/frances-InformationExtraction),
which currently supports [the digitised collections from Data Foundry in National Library of Scotland](https://data.nls.uk/data/digitised-collections/). 
For Encyclopaedia Britannic (EB) collection, each article can be extracted along with its description, while entities inside the description
can not be recognised yet. As the rest of the collections, extraction level remains in page level, which means that it can 
only extract the whole text content of each page, no further than that. To this end, it is essential to balance the level of 
generalisation and specialisation in this Ontology so that it can not only represent the knowledge which can be automatically extracted in great detail,
but also extend easily to adopt new entities and relations that would be extracted in the future.

### _For what types of questions the information in the ontology should provide answers?_

Competence questions (draft)

1. What volumes, editions, or series does a digitalised collection _C_ include?
2. What time period does a digitalised collection _C_ cover? 
3. When was edition _E_, series _S_, or volume _V_ published? 
4. Who published edition _E_, series _S_, or volume _V_? 
5. Who edited edition _E_, series _S_, or volume _V_? 
6. Which genre does a volume _V_ belongs to? 
7. Where was a volume _V_ published or printed? 
8. Which language does a volume _V_ use? 
9. In EB, what articles a volume _V_ include? 
10. Where an EB article _A_ was described (in a page, volume, edition)? 
11. What are the EB articles which appear in all edition? 
12. What EB articles were only appeared once in edition _E_? 
13. What are EB articles related to another EB article _T_? 
14. What are EB articles which has similar description to _T_? 
15. How a term with name _T_ was described in all editions? 
16. What is the text in a page? 
17. What sources the text descriptions of article _T_ or a page _P_ are extracted from? 
18. What is the clean description of term _T_? 
19. What are the descriptions of term _T_ with the highest text quality? 
20. What software was used to extract the description of article _T_ or a page _P_? 
21. What software was used to digitise a document? 

