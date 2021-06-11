---
layout: post
author: Stephan Kurz
title: DHP II Day one wrap-up
license: CC-BY https://creativecommons.org/licenses/by/4.0/deed.de
---

Wrap-up of day one of the ACDH-CH TOOL GALLERY 7.1/Digital Habsburg Platform II "Prosopographical data modeling, Digital Habsburg Platform II" – Round Table


The [event](https://www.oeaw.ac.at/acdh/events/event-series/acdh-ch-tool-gallery-71) started with a warm welcome by [ACDH-CH](https://acdh.oeaw.ac.at/) director Alexandra Lenz, and then swiftly moved on to Matej Đurčo’s concise introduction ([Slides at google](https://docs.google.com/presentation/d/1fZ8Oh3__fL8ZI3qka3LBomFoN8BvDAVW/edit#slide=id.p1)) into the field of data modelling and why it matters for (not only "digital") humanities scholars. 

This was succeeded by the presentations of Daniel Jeller on the [Nuns and Monks – Prosopographical Interfaces, NAMPI](https://nampi.icar-us.eu/) project and Matthias Schlögl on the data model of APIS in general and of the [The Viennese Court. A prosopographical portal, VieCPro](https://viecpro.oeaw.ac.at/) project more specifically. 

The slides of both presentations are available:

- [2021-06-10_ACDH-CH_Tool_Gallery_7-1_Nampi_Daniel_Jeller.pdf](../resources/2021-06-10_ACDH-CH_Tool_Gallery_7-1_Nampi_Daniel_Jeller.pdf)
- [2021-06-10_ACDH-CH_Tool_Gallery_7-1_VieCPro_Matthias_Schloegl.pdf](../resources/2021-06-10_ACDH-CH_Tool_Gallery_7-1_VieCPro_Matthias_Schloegl.pdf) / [reveal.js/GitHub pages](https://sennierer.github.io/viecpro_toolgallery_presentation_2021/), respectively.

Both NAMPI and APIS use their own internal data model for obvious reasons of dealing with very different prosopographical research questions, and moreover with special groups involved with different social domains (monastic versus court-centered) – and both are (working on) providing RDF serialized in a flavour of the [CIDOC CRM](http://www.cidoc-crm.org/) for interoperability goals. 

As if the presentations had not already been substantial enough by themselves, they were still significantly added to by the valuable comments that two external Linked data domain experts contributed in the round table discussion: 

[Victor de Boer](http://www.victordeboer.com/) focused his remarks on the importance of transparency of the provenance of sources, annotations, and of the agents that produce and transpose knowledge (e.g. annotations by an NLP pipeline vs. an intellectual assessment by a domain expert, or conflicting information from biographical natural language sources). Both of the presented data models have means of recording provenance and attribution, yet those are implemented in different ways. 

Victor’s input on data structures and data processing toolchains which have to deal with objects that have different meanings under different circumstances, or with conflicting information in general, shaped the discussion that was to follow in the open floor lateron, with a general consensus on allowing multiple competing "facts" (generally in line with the notions of ["Factoid Prosopography"](https://www.kcl.ac.uk/factoid-prosopography)) that would leave data open for later acts of interpretation to judge which source(s) or agent(s) to trust, use, omit or ignore – over the alternative that would attempt to "fix" the conflict by deciding on a canonical version. (Of course, this infrastructurally neutral approach does not undermine the stance of human agents that are experienced in judging, as they are free to add another layer of statements such as "I have studied this particular issue for ten years." – "That other person making this claim died 120 years ago." – "I concluded that this other statement is not true." [all of which are expressible as RDF triples]).

[Juoni Tuominen](https://research.aalto.fi/en/persons/jouni-tuominen) compared the NAMPI and VieCPro approaches with regard to their communalities and differences – with both being able to serialize into RDF and the CIDOC CRM, and both using external reference identifiers for identification, disambiguation and deduplication of the entities, which is the accepted Linked Open Data way of making assertions of identity between "things". 

In the difference department, Juoni mentioned not only the technology stack, but also the attribution directly and necessarily tied to factoids as they are employed in the NAMPI implementation (with NAMPI being directly implemented in RDF, which VieCPro – using a relational database – has to generate based on the sources of the imported legacy data that may or may not include exact provenance information). While VieCPro employs the generic APIS data model with five basic entity types (person, event, place, work, institution), NAMPI uses its own "monastic life" ontology on top of a generic core ontology; their event-based approach uses "aspects" to add properties to things where APIS employs "mini-events".  

Juoni’s slides will eventually be made available here as well. 

The ensuing round-table discussion included more elaboration with regard to the technical implementation that is planned for the second session on day two, the insight that in general it is much easier to implement positive statements, while uncertainty or the lack of information on a thing is harder to express in an unambiguous way (using RDF, at least), and the centrality of document interpretation acts during any kind of research work or establishment of "knowledge". 

On moderator Thomas Wallnig’s question if and with what amount of effort it were possible to stitch together (prosopographical) data that a) was modelled in the APIS and NAMPI ways, respectively) and b) was external to both in a way that was truly interoperable, the podium quickly agreed (once more) that agreement on one data model ("to rule them all") was fortunately not necessary, but that heterogeneity and polyvocality were possible as long as some common ground was there to be found (align what is alignable, map what’s mappable). 

The takeaway message went back to square one and to Matej’s introduction: **What does one want to say about things?** Research questions prefigurate how we can, should and want to model our data – the rest is up to our decision, plus it would be good to agree on some common identifiers to work against the data silos. Conversion on the way is definitely possible, and accessing data from multiple sources is doable as long as it can be consumed by SPARQL queries! 

(which will be discussed later in the event, that is on [day two](../DHP-II-wrapup-day-two).)

*/Wrap-up: Stephan Kurz, 2021-06-10, late in the day/*
