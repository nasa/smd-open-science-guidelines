# How to make NASA Science Data more FAIR 

Final Draft for Open Comment  \
2024-04-02

# Introduction

The NASA Science Information Policy ([SPD-41a](https://smd-cms.nasa.gov/wp-content/uploads/2023/08/smd-information-policy-spd-41a.pdf)) says SMD-funded data should be Findable, Accessible, Interoperable, and Reusable (FAIR). Moreover, the policy says the NASA Repositories shall align, to the extent practicable, with the [Desirable Characteristics of Data Repositories for Federally Funded Research,](https://www.whitehouse.gov/wp-content/uploads/2022/05/05-2022-Desirable-Characteristics-of-Data-Repositories.pdf) which also emphasize FAIR.

This document describes first steps and initial guidance to help NASA SMD science data repositories make their data more FAIR in the technical sense, based on the [15 FAIR Principles](https://www.go-fair.org/fair-principles/).

It is important to realize at the outset that FAIRness in data curation and system design is not an absolute. It is a spectrum. Improving FAIR-compliance is a continuing journey with incremental steps and continuous improvement.  FAIRness requires investment, so priorities and appropriate levels of service need to be considered

With that in mind, we envision two broad types of technical FAIRness:

- SMD-level FAIRness – a common core of specifications and guidelines that apply to all data archived at SMD repositories

- Division- or discipline-specific FAIRness – more detailed specifications and guidelines that apply to specific divisions, repositories, or thematic areas.

This document focuses primarily on SMD-level FAIRness for data. SMD-level FAIRness for software is an area also in need of work, but software is out of scope for this document. For information about the FAIR Principles themselves, and in particular the expanded details and descriptions being referenced in this guide, see [https://www.go-fair.org/fair-principles/](https://www.go-fair.org/fair-principles/). Much of the interpretation of the principles is based on the [GO FAIR Foundation interpretation](https://www.gofair.foundation/interpretation). 

An initial draft of this document was prepared for the September 2023 SMD Data Repositories Workshop in Boulder, CO. [link to report]. Workshop participants edited and commented on the document during and after the workshop. The SMD Data Repository Standards and Guidelines Working Group then prepared a complete version for broader public comment.

***Unless noted, nothing in this document is a formal requirement. It is a community effort to advance open science within ******NASA******.***

# General Resources for Assessing FAIRness

Many organizations have developed frameworks and criteria for assessing FAIRness. Notable examples include:

- [FAIRsFAIR Assessment tool aka F-UJI](https://www.f-uji.net/?action=test) 

- [GO FAIR Foundation Qualification](https://www.gofair.foundation/criteria)[ ](https://specs.fairdatapoint.org/)

- [FAIR Data Point](https://specs.fairdatapoint.org/)[ FAIR Evaluator](https://www.nature.com/articles/s41597-019-0184-5)[ ](https://www.sciencedirect.com/science/article/pii/S240547121930345X?via%3Dihub)

- [FAIRshake Toolkit](https://fairshake.cloud/)

- [FAIR Data Self Assessment Tool](https://ardc.edu.au/resource/fair-data-self-assessment-tool/)[ ](https://fairdigitalobjectframework.org/)

- [FAIR Digital Object Framework](https://fairdigitalobjectframework.org/)[ ](https://www.go-fair.org/how-to-go-fair/fair-implementation-profile/)

- [FAIR Implementation Profiles](https://www.go-fair.org/how-to-go-fair/fair-implementation-profile/)[ ](https://fairsharing.org/)

- [FAIRsharing standards](https://fairsharing.org/)

- [FAIR Metrics](https://github.com/FAIRMetrics/Metrics)

Currently, only the Open Science Data Repository (OSDR), which includes GeneLab and the Ames Life Science Data Archive (ALSDA) uses [FAIR Evaluator](https://www.nature.com/articles/s41597-019-0184-5) and the [GO FAIR Foundation Qualification](https://www.gofair.foundation/criteria). The NASA Life Sciences Data Archive (not an SMD-funded repository) plans to use  [FAIR Data Point](https://specs.fairdatapoint.org) and [FAIR Evaluator](https://www.nature.com/articles/s41597-019-0184-5). All the repositories funded by other SMD organizations use custom processes largely defined by preexisting standards for their division, discipline, or community. The Astromaterials Data System does use [FAIR Implementation Profiles](https://www.go-fair.org/how-to-go-fair/fair-implementation-profile/) within a custom process.

As we completed the 2023 SMD Workshop, we recognized that we would need to develop a NASA specific metric for at least semi-automated assessment. The Working Group has formed a task force to develop this metric. See the full list of recommendations in the Appendix.

# Making Data FAIR from the Outset

Ideally, data are “born FAIR”. That is, the data adhere to the FAIR principles at the time of creation or ingest into a management system. SMD’s Science Information Policy ([SPD-41a](https://smd-cms.nasa.gov/wp-content/uploads/2023/08/smd-information-policy-spd-41a.pdf)) is primarily geared to data produced after the policy was published (December 2022), so repositories and their stakeholders (including both users and data producers and providers, especially big data providers such as missions and large modeling centers) need to define those requirements and guidelines that enable data to be born FAIR. Metadata standards and vocabularies along with appropriate assessment mechanisms will be essential ([Musen et al. 2022](https://doi.org/10.1038/s41597-022-01815-3)) both for mission data and researcher-provided data. The stated beginning enforcement date of SPD-41a is 31 December 2024. 

Different approaches will be necessary for mission data and research data but both should be FAIR going forward. In this document, we use the  definitions of mission and research data from SMD’s Science Information Policy, and treat data produced by a model as research data.
  We note, however, that during the Repository Workshop there was some confusion as to how the definitions apply to certain cases. For example, ambiguity arises when mission science team members produce additional products derived from the instrument. Some missions/PIs view those as part of the mission, even if the funding to produce them came via a research solicitation. Researcher-provided data can also be very large complex processed data from a NASA mission that was created by researchers who were not at all associated with the mission science team members. SMD will need to address these edge cases as they arise.

When data standards are being defined for new missions or models intended for wide use, there should be an effort to harmonize related legacy data with the new mission or model while respecting past decisions about standards in the new mission or model. Research data will also need more consistent metadata across SMD. The guidance below can provide a basis for that metadata.

NASA already provides some initial [Open-Source Science Guidance for Researchers](https://science.nasa.gov/science-red/s3fs-public/atoms/files/SMD%20Open-Source%20Science%20Guidance%20v2%2020230407.pdf) and is [collaborating with the community to develop guidance for missions](https://doi.org/10.5281/zenodo.8415584). Currently, that guidance includes an [example of an Open Science and Data Management Plan](https://github.com/nasa/smd-open-science-guidelines/blob/main/OSS_Guidance/OSDMP.md#osdmp-templates). Previously, these plans may have been referred to as  Data Management and Access Plans, Data Management Plans, Project Data Management Plans, and Science Data Management Plans.

Of course, SMD repositories hold petabytes of legacy data, which also should become FAIR. The process of increasing the FAIRness of such a large heterogeneous library of data is complex and time-consuming, so this will need to be a long-term and ongoing effort with clear priorities and funding. Repositories can implement some basic practices like those described below to improve FAIRness in the short term while working on greater harmonization of metadata and vocabularies for legacy data over time.

Finally, making data FAIR is a community wide effort. The [NASA TOPS Open Science modules](https://nasa.github.io/Transform-to-Open-Science/open-science-101/) contain materials designed to educate the community on Open Science, including how to increase the FAIRness of data and other mission and research artifacts. Some relevant topics covered by the curriculum are:

- Familiarity with data management and software management plan best practices and resources,

- How to find and identify community accepted data and software repositories,

- How to openly license and share FAIR data and assign a DOI, and

- Applying a permissive license, sharing open-source software, and assigning a DOI.

The modules were released to the public in December 2023. This document recommends these modules to the community as an excellent place to learn the basic skills of how to create data that is FAIR.

# Suggested SMD-wide Actions and Guidance for each Principle

This section gets into the specifics of what a repository needs to do to make their data FAIR. For each of the FAIR principles we provide:

- **Interpretation and Context:** an SMD-wide interpretation of what the principle means and how it applies to SMD repositories.

- **First Steps**: things that repositories can do now to address the principle. More resources may be required to implement the step, but there is a clear and achievable action to take.

- **Recommendations for next steps:** are recommendations for repositories or other NASA entities that define further actions necessary to meet the principle.

- **Resources:** documents and tools that help repositories implement the first steps or define the next steps. NASA guidance and resources are highlighted when available.

The Appendix provides a single list of all the recommendations from the report.

## Findable

### F1: (meta)data are assigned a globally unique and persistent identifier

#### Interpretation/Context

SMD adopts the US National Science and Technology Council definition of  a globally unique and  persistent identifier: “a digital identifier that is globally unique, machine resolvable, and with an associated metadata schema that identifies an entity (e.g., individual researcher, digital research object) in perpetuity and is used to disambiguate as well as build associations between entities.” ([NSTC, 2023](https://www.whitehouse.gov/wp-content/uploads/2022/01/010422-NSPM-33-Implementation-Guidance.pdf))

Note the identifier might be associated with the target data itself, or with the metadata that describes the target. There should be clear linkage between the two, as described in F3.

#### First Steps

- Assign a DOI at a logical and useful level of data collection, especially when enabling citation and reference.

- Consider assigning IDs at lower levels of granularity or enabling PIDs to be assigned and maintained for queries as appropriate. These need not be DOIs. [Archive Resource Keys (ARKs)](https://arks.org/), [Universally Unique Identifiers (UUIDs)](https://en.wikipedia.org/wiki/Universally_unique_identifier) or locally resolvable unique identifiers are also suitable choices.

#### Recommendations for Next Steps

- There is a clear need for further guidance on the assignment of PIDs for different use cases. Such guidance needs to be developed, possibly by a SMD-wide working group.

- The guidance below on when to assign a PID to a dataset produced by a model needs to be discussed for possible SMD-wide adoption.

#### Resources and Guidance

NASA Guidance:

- [How to register a DOI for Data Citation](https://github.com/nasa/smd-open-science-guidelines/blob/main/guidance/guideline001_doi_registration.md) provides guidance on responsibilities and processes for assigning DOIs to data cited in literature, including  additional references and guidance for different divisions).

- [NASA Digital Persistent Identifier (DPI) Services](https://nasa.sharepoint.com/sites/dpiservices) (NASA Credentials required)

Other Guidance:

- [Joint Declaration of Data Citation Principles](https://doi.org/10.25490/a97f-egyk)

- [Data Citation of Evolving Data: Recommendations of the RDA Working Group on Data Citation](https://doi.org/10.15497/RDA00016) and the explanatory paper by [Rauber et al. (2021)](http://dx.doi.org/10.1162/99608f92.be565013).

- When to assign a PID to a dataset produced by a model ([https://modeldatarcn.github.io/](https://modeldatarcn.github.io/)). 

- [DataCite Support](https://support.datacite.org/)

### F2: data are described with rich metadata

#### Interpretation/Context

The concept of *rich metadata* relates specifically to expanding the scope and context of data discovery well beyond the initial mission team or disciplinary community (see F4). Such metadata are consistent enough and expansive enough that a user (using generic search tools) should be able to find data and assess their suitability for use in their context without knowing in advance what data exist, where they are curated, or what their original use and purpose were. Practically speaking, it often means including explicit values and concepts that might be considered obvious, or “taken as read” in the home repository and thus omitted from the metadata as unnecessary.

“Thus, this principle encourages data providers and domain experts to consider the various facets of search that might be employed by a user of their data, and to support those users in their discovery of the resource. To enable both global and local search engines to locate a resource, generic and domain-specific descriptors should be provided that can be exposed to indexing by the relevant search facilities (See F4).” - [GO FAIR Foundation](https://www.gofair.foundation/f1). 

Defining the rich metadata necessary to enable interdisciplinary search is especially challenging. More user studies are necessary to define those requirements. At the same time, metadata richness comes at a cost, so priorities and appropriate levels of service need to be considered while also continuing to explore how improved interfaces and machine learning approaches can automate the generation of more discovery metadata.

#### First Steps

- For data sets with DOIs, provide as complete metadata as possible when the DOIs are minted according to the DataCite metadata schema, and communicate any metadata changes to DOI registries as soon as possible. (Note: even a full complement of  DataCite metadata is just a minimum. Repositories should make fuller metadata available through their landing pages and access systems. See I3 and R2.)

- Annotate appropriate data landing pages with schema.org markup, including JSON-LD for linked data.

- Provide necessary information for the developing Science Discovery Engine core metadata elements.

#### Recommendations for next steps:

- Establish a working group to develop SMD-level guidance on how common metadata standards are developed: what needs to be included, who is at the table, how it is governed, what the means of community input are, means of development, update, and versioning., etc.

#### Resources and Guidance

- [Science Discovery Engine core metadata elements]([https://www.google.com/url?q=https://docs.google.com/spreadsheets/d/18-6ZToXJPw_rKF0nb9Pua1VANMu-7Lec7183P-nDIZs/edit?usp%3Dsharing&sa=D&source=docs&ust=1705439530011685&usg=AOvVaw2biPLKdYjrXTXdo1l2JiWi](https://docs.google.com/spreadsheets/d/18-6ZToXJPw_rKF0nb9Pua1VANMu-7Lec7183P-nDIZs/edit?usp=sharing) and crosswalks across divisions and DCAT3 (in development)

- The [OAIS Reference Model (ISO 14721) provides](http://www.oais.info/) (developed by NASA) is a general conceptual model for descriptive metadata. 

- Ruth Duerr’s workshop tutorial on schema.org [https://doi.org/10.5281/zenodo.10251814](https://doi.org/10.5281/zenodo.10251814) 

- [Science On Schema.Org (SOSO) Guidance Documents](https://github.com/ESIPFed/science-on-schema.org)

- [DataCite Support](https://support.datacite.org/)

- Starr et al. (2015)  Achieving human and machine accessibility of cited data in scholarly publications. *PeerJ Computer Science*. [https://doi.org/10.7717/peerj-cs.1](https://doi.org/10.7717/peerj-cs.1) 

### F3: metadata clearly and explicitly include the identifier of the data it describes

#### Interpretation/Context

This aspect of FAIRness is a practical one, in that it explicitly notes that a unique identifier that is not present is not useful. It is a reminder to curators that the globally unique, persistent identifier *must *be propagated to the metadata for the target data  itself, not merely cataloged in an institutional database.

#### First Steps

- Ensure the DOI/identifier is included in the data product metadata as well as embedded in the landing page in human-readable and machine-readable formats. Typically resolution protocol should be included with the identifier (e.g., https://doi.org/…) 

- Ensure an identifier is included in the DOI metadata directing to detailed product metadata. Use the RelatedIdentifier field with relationType IsDescribedBy.

- Ensure the DOI/identifier is included in the initial metadata returned in response to user queries through public interfaces (be they web-based or API).

#### Resources and Guidance

- [Science On Schema.Org (SOSO) Guidance Documents](https://github.com/ESIPFed/science-on-schema.org)

- [FAIR DataPoint specifications](https://specs.fairdatapoint.org/fdp-specs-v1.2.html)

- [DataCite Support](https://support.datacite.org/)

### F4: ​​(meta)data are registered or indexed in a searchable resource

#### Interpretation/Context

“Searchable resource” is not simply a repository’s search interface, which requires a machine to know of its existence. Those data are only findable to users who already know where the data are located. This principle is concerned with searchable resources that aggregate metadata from multiple repositories.

Data should be discoverable in discipline specific services like the [Earth Science] Common Metadata Repository (CMR) or the Planetary Data System (PDS); broad research data systems like DataCite Commons, the NASA Science Explorer (SciX) and Science Discovery Engine (SDE), and Data.gov; and generic search engines like Bing or Google. 

Some of these systems crawl the web to identify and index relevant web pages, some require active submission by the curators to register their metadata. Either way, the scope of content is greater than any single repository, and typically encompasses a number of (possibly related) disciplines. The responsibility for collecting and publishing metadata that supports these broader databases typically falls on the curator.

#### First Steps

- Register data DOIs with DataCite.

- Ensure your (meta)data are indexed in all registries/indexes appropriate to the discipline(s) interested in your repository’s data (CMR, PDS, HDRL, OSDR…)

- Annotate data set landing pages with schema.org markup so that they are indexed by all major search engines.

- Provide auto generated citation text in common formats like bibtex, RIS, and txt on data set landing pages for authors to use when citing the data.

#### Resources and Guidance

- [How to register a DOI for Data Citation](https://github.com/nasa/smd-open-science-guidelines/blob/main/guidance/guideline001_doi_registration.md) (includes additional references and guidance for different divisions and more details).

- [Science On Schema.Org (SOSO) Guidance Documents](https://github.com/ESIPFed/science-on-schema.org)

## Accessible

### A1. (meta)data are retrievable by their identifier using a standardized communications protocol

#### Interpretation/Context

This principle is directly concerned with the operational specifics of acquiring data from a repository once it is found. “Accessible” in this context is not the same as “Open”. While most SMD data are open, some are not.
This principle ensures that no additional access barriers are encountered once appropriate permissions have been granted.

“The ‘standardized communication protocol’ is critical here. Its purpose is to provide a predictable way for an agent to access a resource, regardless of whether the access to the content of the resource is open or restricted, and regardless of whether that access is automated or aided by human action (e.g., send your request for access by email or telephone).”  - [GOFAIR Foundation](https://www.gofair.foundation/a1)

The FAIR principles are equally applicable to all data regardless of how open they are. For access, this principle concerns the transparency of data access mechanisms. The point is to specify clearly in a machine readable way what is required to access the data.

#### First Steps

- Implement a DOI retrieval option in the local interface.

- Implement a DOI retrieval option in the API, SFTP, and other programmatic interface(s).

### A1.1 the protocol is open, free, and universally implementable

##### Interpretation/Context

*The protocol* is the method by which the data can be parsed into packets, transmitted over the internet, and recomposed at the destination. Often this is either HTTP/HTTPS or FTP/SFTP. *Open, free, and universally implementable* means that the specification is publicly available free of charge, can be implemented without charge or restriction, and can be implemented on any system architecture that could be reasonably expected to handle the process.

Most SMD repository access protocols are currently open. An open question is how to interpret this principle in a cloud computing context.

#### First Steps


- If the only interface(s) requires human interaction, prioritize API development.

### A1.2 the protocol allows for an authentication and authorization procedure, where necessary

#### Interpretation/Context

This principle relates directly to the difference between “FAIR” and “Open”. To be FAIR, the *access protocol* must be open, but the *data *need not be open. An “open” access protocol may deny access to the data by unauthorized users. Because the protocol itself is open, a machine or user can at least attempt to access the data and either be allowed or rejected for a specific and clearly stated reason (e.g. ITAR, PII, embargos, etc.). 

This principle also serves to encourage curators and data creators to make metadata available for data that might be restricted. The existence and availability requirements of the data can be documented without requiring open access.

#### First Steps

- The Chief Science Data Office should finalize guidance on user authentication and identity management.

### A2. metadata are accessible, even when the data are no longer available

#### Interpretation/Context

Data may be deleted by design or accident. For example, an early version of a data set may be retired when replaced with a new improved version. “Given that those data may have been used and are referenced by others, it is important that consumers (including machines) have, at the very least, access to high quality and machine actionable metadata that describes those resources sufficiently to minimally understand their nature and their provenance, even when the relevant data are not available anymore. This principle relies heavily on principle F3 (the metadata record contains the identifier of the data), because in the case where the data are no longer available, there must be a clear and precise way of discovering its historical metadata record.” ([GOFAIR Foundation](https://www.gofair.foundation/a2)). This “Tombstone metadata" should tell a prospective user what happened to the data and how to request access if it is still available in some form.

#### First Steps

- Repositories should develop and implement policies and procedures to provide “tombstone pages” and indexing in appropriate registries for deleted data, including outdated versions of a dataset. 

#### Resources and Guidance

- [NASA Digital Persistent Identifier (DPI) Services](https://nasa.sharepoint.com/sites/dpiservices) (NASA Credentials required)

- [DataCite Support](https://support.datacite.org/)

- [Joint Declaration of Data Citation Principles](https://doi.org/10.25490/a97f-egyk)

## Interoperable

### I1. (meta)data use a formal, accessible, shared, and broadly applicable language for knowledge representation.

#### Interpretation/Context

The question of *Interoperability* is very complex especially when trying to span across all the disciplines addressed by NASA over many decades. It is likely the most difficult aspect of FAIR. Nonetheless, there are some common technical fundamentals to build from.

This principle requires that metadata be described in a common machine interpretable language regardless of detailed metadata semantics or syntax. [Jacobson et al (2020)](https://doi.org/10.1162/dint_r_00024) describe it well:



The key consideration in this regard is that FAIR speaks to the ability of data to be reused by a generic agent, rather than a community-specific agent. This is most easily accomplished by making the knowledge available in the most widely used format(s), even if this means duplication of the information in the community-specific format.

The most widely-accepted choice to adhere to this principle, at the present time, is the Resource Description Framework (RDF) which is the W3C's recommendation for how to represent knowledge on the Web in a machine-accessible format. Other choices may also be acceptable, for instance when they are already in widespread use within a given community. In that case, it would be helpful for the community to also provide a “translator” between their preferred format, and a more widely used format such as RDF.

NASA may already be using a limited number of languages and metadata formats. Examples include [RDF](https://www.w3.org/RDF/), SKOS, OWL-DF, various XML representations, JSON-LD, schema.org markup, and others. Repositories will need to provide the same metadata in multiple formats or provide translators, but we should be able to agree on a fairly limited set.

#### First Steps

- Establish a TG to identify current practice and recommend common practice (e.g. development of the metadata format translators mentioned above). Consider shared standards including DataCite, DCAT, and schema.org. Ideally this would be done in collaboration with other agencies.

#### Resources

- [Science Discovery Engine core metadata elements](https://docs.google.com/spreadsheets/d/18-6ZToXJPw_rKF0nb9Pua1VANMu-7Lec7183P-nDIZs/edit?usp=sharing) and crosswalks across divisions and DCAT3 (in development)

- Mapping between Schema.org and DataCite: [https://doi.org/10.5281/zenodo.7661398](https://doi.org/10.5281/zenodo.7661398) 

- Mapping between Schema.org and 14 metadata models: Mingfang Wu, Stephen M. Richard, Chantelle Verhey, Leyla Jael Castro, Baptiste Cecconi, Nick Juty; An Analysis of Crosswalks from Research Data Schemas to Schema.org. Data Intelligence 2023; 5 (1): 100–121. doi: [https://doi.org/10.1162/dint_a_00186](https://doi.org/10.1162/dint_a_00186) 

### I2. (meta)data use vocabularies that follow FAIR principles

#### Interpretation/Context

‘Vocabularies' are the “methods that unambiguously represent concepts that exist in a given domain. The use of shared, and formally structured (principle I1), sets of terms is an essential part of FAIR. Terminology systems, including flat ‘vocabularies’, hierarchical ‘thesauri’ and more granular specifications of knowledge such as data models and consistently structured ontologies, play an important role in community standards.” – [GOFAIR Foundation](https://www.gofair.foundation/i2)

NASA has been an active player in this area and has developed or adopted multiple ‘vocabularies’. These vocabularies are of varying degrees of formality and do not generally adhere to FAIR principles, but they provide a solid foundation. Examples include the Science Keywords of the Global Change Master Directory (GCMD) and the Unified Astronomy Thesaurus (UAT).

This is probably the most difficult principle because different disciplines and ways of knowing provide such different conceptual models. NASA, however, may be uniquely positioned to codify standards for many space science and some Earth science disciplines.

#### First Steps

- At a base level, repositories should use the [W3C Data Catalog Vocabulary (DCAT)](https://www.w3.org/TR/vocab-dcat-3/)[ ](https://www.w3.org/TR/vocab-dcat-3/)to describe their holdings.

- Repositories should identify the vocabularies that are relevant to their discipline, broadly accepted, and generally machine actionable. They should share these broadly with SMD, ideally using a standard for capturing vocabularies. For example, ISO/IEC 11179, Volume 3, provides a comprehensive schema for a metadata registry. (When a discipline does not have an established vocabulary, effort should be made to add the needed terms to a currently existing vocabulary rather than creating a new one.)

- Repositories should develop and implement plans to integrate these vocabularies into their curation workflows.

#### Recommendations for Next Steps

- Where possible, repository staff should actively participate in the development of community standards (e.g. for vocabularies, metadata, data formats, and so on). Repositories should also maintain a general awareness of standards used across different divisions and user communities (e.g., through the annual repository workshop) to identify opportunities for overlap and lessons learned. 

- SMD should develop a repository of vocabularies in use and explore ways to ensure they are FAIR..

#### Resources

- [W3C Data Catalog Vocabulary (DCAT)](https://www.w3.org/TR/vocab-dcat-3/)

- [I-ADOPT Framework Ontology](https://i-adopt.github.io/)

- [Global Change Master Directory Keywords](https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords) (Earth Science)

- The [Unified Astronomy Thesaurus (UAT)](https://astrothesaurus.org/)

- [https://github.com/DOI-DO/dcat-us/wiki/FAIR-Vocabularies](https://github.com/DOI-DO/dcat-us/wiki/FAIR-Vocabularies) 

### I3. (meta)data include qualified references to other (meta)data

#### Interpretation/Context

A *reference* in this context is an association between the resource in question and a different resource, in the same repository or elsewhere, typically using a persistent identifier. A *qualified reference* includes an indication of *why* the association has been made, that is, the nature of  relationship between the two resources.

The idea is that data or metadata should not exist in a silo and generally need to be connected to other resources to be fully meaningful and to enable services for the data, and that connection must be described. We need both the noun *and the verb. *Qualified references could include authorship, citations to or from the literature, linkages to different versions of the (meta)data, relations describing provenance (e.g. ‘derived from’, see R1.2), contextual relationships (e.g. ‘is part of’), linkages to related information (e.g. instrument metadata), or many other things. Generally the more references the better, especially when using machine actionable identifiers and standard vocabularies.

#### First Steps

- Add ORCIDs to product metadata for data creators and other relevant people.

- Add known identifiers to related publications and software in product metadata.

- Add [SPDX](https://spdx.org/licenses/) license identifiers to product metadata 

- Add organizational identifiers such as to product metadata wherever appropriate (e.g., [ROR](https://ror.org),[ ](https://grid.ac/)[GRID](https://grid.ac/), or ISNI identifier, or a more specific[ ](https://api.crossref.org/funders/)[Funder ID](https://api.crossref.org/funders/) from the[ ](https://www.crossref.org/services/funder-registry/)[Crossref Funder Registry](https://www.crossref.org/services/funder-registry/))

#### Guidance

- The [SPDX License List](https://spdx.org/licenses/) is a list of commonly found licenses and exceptions used in free and open or collaborative software, data, hardware, or documentation. The SPDX License List includes a standardized short identifier, the full name, the license text, and a canonical permanent URL for each license and exception.

## (Re)Usable

### R1. meta(data) are richly described with a plurality of accurate and relevant attributes

#### Interpretation/Context

For the purposes of avoiding confusion in the following discussion:

- The *data* are described by the *metadata*.

- The *metadata* are described by a *schema *and* vocabularies *(formal or informal).

- *Richly*, *plurality*, *accurate*, and *relevant* are acknowledged to be subjective and highly context-dependent terms.

Overall, this is the most broadly scoped principle and one where curators have room for continued improvement. “The term ‘plurality’ is used to indicate that the metadata author should be as generous as possible, not narrowly presuming who the secondary consumers might be, and therefore provide as much metadata as possible to support the widest variety of use-cases and agent needs.” ([GOFAIR Foundation](https://www.gofair.foundation/r1))

The first two sub-principles quantify specific aspects of “richness” and “plurality” that have the greatest and most universal impact on Reusability*.* The third sub-principle is perhaps where curators have the most scope for serving their target communities and beyond.

### R1.1. (meta)data are released with a clear and accessible data usage license

#### Interpretation/Context

The purpose of this principle is for machines to understand what they can *legally *do with the data while respecting intellectual property rights. 

Most NASA science data should be open. [SPD-41a ](https://smd-cms.nasa.gov/wp-content/uploads/2023/08/smd-information-policy-spd-41a.pdf)states: 

Publicly available SMD-funded data shall be reusable with a clear, open, and

accessible data license.

a) If there are no other restrictions, SMD scientific data should be released with a Creative Commons Zero license. Legal limitations on data may include, but are not limited to, limited rights data, data governed by incompatible licenses, or data containing restricted information. Seek specific advice from the Chief Science Data Office or Intellectual PropertyCounsel, as needed.

Further guidance at [https://science.data.nasa.gov/license/](https://science.data.nasa.gov/license/) states:

Scientific data shared via NASA data repositories currently falls into three categorizations for licenses:

1. The data has a license provided with it or is labeled with its license. The data or data collection may be labeled with a license as part of the metadata. The licenses and terms of usage may be provided on the website, in the documentation of the data, or via other methods.

2. Unless the data file is marked with a restrictive notice or license, data that is provided from a NASA-led mission including observations, engineering, calibration, and auxiliary data are licensed as [Creative Commons Zero](https://gcc02.safelinks.protection.outlook.com/?url=https%3A%2F%2Fcreativecommons.org%2Fpublic-domain%2Fcc0%2F&data=05%7C01%7Candi.thomas%40nasa.gov%7C44ba463a7fe04d182f2308dbc4f4108b%7C7005d45845be48ae8140d43da96dd17b%7C0%7C0%7C638320324743373232%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&sdata=fYHnkA0yR0I5UlUH%2FFpfwydjPCoqTRFmq8ysd5%2Bu3jI%3D&reserved=0). There are no restrictions on the usage of these data.

3. For all other data, the data are provided as is and NASA makes no warranty whatsoever or representations regarding usage. NASA may not be the original source of data and thus users are encouraged to validate the source and associated usage rights of the data.

Note that while CC0 does not formally *require* data citation, it does encourage respect for ethical norms in the use of data including data citation as encouraged by SPD-41a. A major reason for using CC0 (apart from US legal requirements) is that the attribution requirement of CC-BY can hinder automated reuse. Research data may have a license other than CC0. It depends on the language in the contract or grant.

#### First Steps

- Provide a recommended citation for all data both on the interface and in the metadata. This citation should preferably be available in multiple formats through an interface and an API (e.g. BibTeX for structure vs APA for format).

- For data with existing licenses or waivers, provide machine readable metadata (eg. schema.org or RDFa) describing the license and any restrictions.

- Add [SPDX](https://spdx.org/licenses/) license identifiers to product metadata

- Label unrestricted data and their metadata with a machine readable CC0 badge.

#### Recommended Next Steps:

- Consider documenting the norms of expected use which can be linked from the CC0 badge.

#### Resources

- [CC0 FAQ](https://wiki.creativecommons.org/wiki/CC0_FAQ)

- [RDA-CODATA Legal Interoperability of Research Data: Principles and Implementation Guidelines](https://doi.org/10.5281/zenodo.162241) or why data providers should generally favor CC0 over CC-BY.

- [Science On Schema.Org (SOSO) Guidance Documents](https://github.com/ESIPFed/science-on-schema.org) on how to reference licenses using the [SPDX License List](https://spdx.org/licenses/)  – a list of commonly found licenses and exceptions used in free and open or collaborative software, data, hardware, or documentation. The SPDX License List includes a standardized short identifier, the full name, the license text, and a canonical permanent URL for each license and exception.

- [SPD-41a](https://smd-cms.nasa.gov/wp-content/uploads/2023/08/smd-information-policy-spd-41a.pdf)

### R1.2. (meta)data are associated with detailed provenance

#### Interpretation/Context

Basic *provenance* for a data product includes the source, date of creation, and creators. Additional metadata related to provenance might include things like instrumentation, data collectors, reduction state, software used, source products, and so on. Rich provenance metadata enables users to select data more likely to be applicable to their investigation, or to assess the likely quality of a data product of interest. Provenance that includes qualified references to other data products or publications in the professional literature can lead users to discover new information relevant to their research, or reveal information about their target data set that was not previously known.

#### First Steps

- For data products derived from other data, include references (with PIDs) to the source data in the  product metadata.

- Add ORCIDs to product metadata for data creators and other relevant people.

- Add organizational identifiers such as to product metadata wherever appropriate (e.g., [ROR](https://ror.org),[ ](https://grid.ac/)[GRID](https://grid.ac/), or ISNI identifier, or a more specific[ ](https://api.crossref.org/funders/)[Funder ID](https://api.crossref.org/funders/) from the[ ](https://www.crossref.org/services/funder-registry/)[Crossref Funder Registry](https://www.crossref.org/services/funder-registry/))

#### Recommendations for Next Steps

- Repositories should define and publish best practices for describing data provenance and strongly encourage data providers to adhere to these best practices.

- ESD has an [Earth Science Data Preservation Content Specification](https://www.earthdata.nasa.gov/esdis/esco/standards-and-practices/preservation-content-spec) which may be useful to other divisions. 

#### Resources

- [Science On Schema.Org (SOSO) Guidance Documents](https://github.com/ESIPFed/science-on-schema.org)

- [DataCite metadata model](https://schema.datacite.org/)

- [Joint Declaration of Data Citation Principles](https://force11.org/info/joint-declaration-of-data-citation-principles-final/)

- [DOI Citation Formatter](https://citation.crosscite.org/)

- [CiteAs](https://citeas.org)

### R1.3. (meta)data meet domain-relevant community standards

#### Interpretation/Context

This is one of the more challenging principles. Trade-offs are required between serving a well-defined community vs. enabling reuse for broader and less homogeneous communities. Data format, terminology, and metadata standards tailored for one community can represent a barrier to another and even exclusion for a third.

The OAIS Reference Model says that repositories should serve a ‘Designated Community – an identified group of potential Consumers who should be able to understand a particular set of information. The Designated Community may be composed of multiple user communities. A Designated Community is defined by the Archive and this definition may change over time.’

Adapting to changes in a designated community usually requires additional resources for repositories. Any assessment of FAIRness needs to take into account the community the specific repository is intended to serve.

#### First Steps

- Each repository should clearly define their designated communities, while defining a plan for expanding that community.

- Each division should clearly specify the metadata standards and vocabularies they currently use or require in a single, ideally machine-readable, location.

#### Recommendations for Next Steps

- Each repository should document how it mitigates (beyond one community) the barriers other communities face, ideally done in collaborations with repositories representing closely related communities.

#### Resources and Guidance

- [OAIS Reference Model (ISO 14721)](http://www.oais.info/)

# FAIR Assessment

The sections above describe initial work that repositories can undertake (funding permitted) to make their data more FAIR. It became apparent at the workshop, however, that we are not yet at a point where we can formally and objectively assess the FAIRness of a data set. The SMD Repositories WG will establish two task groups to help address this issue. One group will define a FAIR metric. The other will focus on common metadata requirements. The work of these groups needs to be more precisely scoped, but the list below includes topics for consideration that were identified during the workshop and subsequent discussion.

- Consider developing a common SMD-wide base metadata schema to better accommodate mission and research data, ensuring the added fields are generic across the SMD divisions, such as funding information. This could be based on DataCite or DCAT with some additional requirements.

- Create a standard FAIR assessment metric and tool, building on those that already exist, that is easy to use and generic to all SMD divisions that determines a FAIR score based on a comparison of the provided metadata with the improved version of the DataCite metadata schema.

- Collaborate with the community via workshops to determine what minimum FAIR score should be required for research and mission datasets, taking into account the desired capabilities of the metadata provided and the burden required of the data provider. This is especially important when considering research data since the time required to complete those tasks are generally not covered by their grants.

- Develop software to make the SMD-wide minimum metadata schema extensible by each SMD division and repositories.

- Design the standard FAIR assessment tool’s backend to have a shared core but also enable discipline-specific extensions.

- Reduce the repetitiveness of metadata creation by developing automated crosswalks and mappings (e.g. the mapping between DataCite and schema.org done by RDA) between this minimum metadata standard and the SMD division and repository -specific metadata standards.

- Some NASA repositories I (e.g., NSIDC) define explicit levels of service for their individual data sets ([https://www.earthdata.nasa.gov/engage/new-missions/level-of-service](https://www.earthdata.nasa.gov/engage/new-missions/level-of-service)). [CoreTrustSeals.org](https://doi.org/10.5281/zenodo.8083359) has recently published a discussion paper on the topic (especially for data submitted in support of a publication). Defining levels of service can help providers, curators, and users have  an agreed understanding of how FAIR a data set may expected to be. Repositories and providers need to work together to define expected levels of service. 

- Collaborate through NASA with InvenioRDM, [Zenodo’s next generation platform](https://blog.zenodo.org/2022/12/07/2022-12-07-zenodo-on-inveniordm/), by creating SMD division and repository -specific collections on that platform to accommodate datasets of metadata quality lower than required by a given relevant repository.

- Create a user interface similar to [TurboTax](https://turbotax.intuit.com/) for metadata creation, including explanations, motivations, and examples for each requested item.

- Develop a chatbot to help answer user questions and incorporate into the interface (e.g. the [PyHC chatbot](https://zenodo.org/doi/10.5281/zenodo.8408825)).

- Include links to help desks in the interface.

- Incorporate the standard FAIR assessment tool into this user interface to report the current FAIR score just as TurboTax reports the current expected tax fees/refund.

- Design this user interface backend to be extensible by the SMD divisions and repositories.

- “Richness” is necessarily discipline specific. SMD divisions and repositories should publish the standards they use and coordinate APIs where appropriate (e.g. DataCite). As appropriate, they should also publish an accepted level of service for each data set.

- Incorporate the use of AI/ML tools to increase the richness of metadata during generation and curation, such as suggestion technology and even metadata drafting.

- Create a shared library of these and other metadata creation and curation tools for better collaboration on streamlining and where possible automating the creation and curation of metadata for both curators and metadata providers.

- Define specific machine-understandable data-access restrictions – ITAR, PII, etc.

# Acknowledgements

2023-09-18: This document was originally drafted by the program committee for the 2023 Annual NASA Open Science Repositories Workshop:

- Mark Parsons (OCSDO) [https://orcid.org/0000-0002-7723-0950](https://orcid.org/0000-0002-7723-0950)   

- Robert Downs (ESD) [https://orcid.org/0000-0002-8595-5134](https://orcid.org/0000-0002-8595-5134) 

- Samrawit Gebre (BPS) [https://orcid.org/0000-0002-8963-4856](https://orcid.org/0000-0002-8963-4856) 

- Julie Imig (APD) [https://orcid.org0000-0002-8595-5134](https://orcid.org0000-0002-8595-5134) 

- Lan Jian (HPD) [https://orcid.org/0000-0002-6849-5527](https://orcid.org/0000-0002-6849-5527) 

- Anne Raugh (PSD) [https://orcid.org/0000-0002-8300-9443](https://orcid.org/0000-0002-8300-9443)

2024-02-20: The Repository WG prepared a complete draft based on the input from the community during the workshop and afterwards.


- Lorella Angelini

- Daniel Berrios

- Kaylin Bugbee

- Bobby Candey

- David Ciardi

- Steve Crawford

- Bob Downs

- Robin Fergason

- Steve Hughes

- Sara Lubkin,

- Tom Morgan

- Susan Mullally

- Jordan Padams

- Mark Parsons

- Ge Peng

- Rebecca Ringuette

- Erich Reiter

- Brian Thoma

- 
# Appendix — Summary of Recommendations

Once the document is generally agreed on, this will be a summary list of all the recommendations in the report.

# Acronyms

**OSDR**: Open Science Data Repository

**SMD**:* *Science Mission Directorate

[more to be added later]
