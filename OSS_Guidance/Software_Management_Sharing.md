# Software Management and Sharing
Consistent with the principles of open-source science, software developed using SMD funding shall be made publicly available through methods that are transparent, inclusive, accessible, and reproducible. The open sharing of research software improves the reproducibility of research, enables other scientists to use and build upon software developed using public funds, and allows the researchers who share the software to be cited and recognized for the impact of their work.  As software has become increasingly more important to the scientific process, scientific manuscripts do not always capture all of the nuance that is in the source code that supports the paper.  Sharing the software ensures that others can better understand and reproduce the results reported in the manuscript. 

This page contains supplemental guidance for researchers to support the implementation of requirements for software management and sharing established by SPD-41a. In addition to these pages, researchers should reference the guidance provided in the software policies and guidance provided by their relevant divisions.

## Software in Scope of SPD-41a
Software is defined as computer programs, including source and object code, that provide users some degree of utility or service. Scientific software in scope of SPD-41a is software that provides users some degree of scientific utility or produces a scientific result or service. Further definitions and examples of software are provided in [Types of Research Software and Expectations for Sharing](Research_Software_Types.md).  The guidance provided here is most relevant for research software that is produced by investigations funded via SMD research awards. This software should be developed and released as described in the project’s software management plan. 

Software developed only for preliminary analysis, plans for future research, or communication with colleagues is not required to be released.

Restricted software, that is software that is subject to specific laws, regulations, or policies (e.g., Export Administration Regulations (EAR), International Traffic in Arms Regulations (ITAR), intellectual property laws, license restrictions) that would prevent the release of this information, is exempt from the requirements for making software publicly available. Section II-C of SPD-41a lists additional laws, regulations, and policies that generate exceptions to software sharing requirements. This includes scientific software for which release is limited by patent rights, as described in the governing document of the funding mechanism, including
“Patent Rights for Small Business Firms and NonProfit Organizations.”

Commercial software, that is software that is produced for the purposes of sale and includes software that would be classified as commercial-off-the-shelf (CoTS), is not included in the types of software that must be released as part of research awards. Software developed in a proprietary or commercial language, such as IDL or MATLab, is expected to be released if allowed by the license. 

## Software Management Plans
All SMD-funded scientific activities that are expected to produce software shall include a software management plan (SMP) describing how software will be managed, preserved, and released to comply with the requirements of SPD-41a. The software management plan may be one component of a broader [OSDMP](OSDMP.md). Though not required under SPD-41A, the OSDMP will be a required component of many proposals for SMD funding starting with ROSES-2023.

At a minimum, a software management plan for SMD-funded research should include:
* Descriptions of the software expected to be produced from the proposed activities, including types of software to be produced, how the software will be developed, and the addition of new features or updates to existing software.  This can include the platforms used for development, project management, and community-based best practices to be included such as documentation, testing, dependencies, and versioning. 
* The repository(ies) that will be used to archive software arising from the activities and the schedule for making the software publicly available 
* Description of software that are subject to relevant laws, regulations, or policies that exclude them from software sharing requirements 
* Roles and responsibilities of project personnel who will ensure implementation of the software management plan

Software management plans should reflect the practices of specific research communities, and SMD Divisions and/or ROSES program elements may provide additional guidance on format and content. 

## Timeline for Sharing Software
Scientific software resulting from SMD-funded scientific activities shall be made publicly available, to the extent allowed by applicable law and existing NASA policies, according to the following timeline:
1. Scientific software needed to validate the scientific conclusions of peer-reviewed manuscripts resulting from SMD-funded scientific activities shall become publicly available no later than the publication date of the corresponding peer-reviewed article. This includes software required to derive the findings communicated in figures, maps, and tables, as well as scientifically useful software from models and simulations.
2. Any scientifically useful software associated with a SMD research award shall be made publicly available by the end of the period of performance, whether or not the software would be needed to validate the scientific conclusions of a peer-reviewed publication. 
   
## Where to Share Software
 Software must be shared and archived in locations that ensure its accessibility and preservation. Researchers should follow the guidance for how to share software as described in the relevant solicitation or under the division software policies if available. 

If there is no specific guidance on how to share software, options for where to share software can include:
* In the supplemental material of a publication. This is ideal for small scripts, notebooks, or spreadsheets that include calculations necessary for reproducing the paper.
* Publishing the source code in a software specific journal.
* If shared on a version controlled platform (e.g. [GitHub](https://github.com/)), it is also important to archive the software at a designated repository.  
* [GitHub has integration with Zenodo](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content) to make it easy to create an archived copy of the software.
* In public repositories already used in the community such as [Zenodo](https://zenodo.org/), [Astrophysics Source Code Library](https://ascl.net/), and [Software Heritage](https://www.softwareheritage.org/). 

The method for archiving and sharing the software should be described in the Software Management Plan.  

## General Expectations for Open-Source Software
Unrestricted software developed using SMD-funding is expected to be shared openly. There are many different types of software and the expectations for software sharing are different for missions and researchers (See [Types of Research Software and Expectations for Sharing](Research_Software_Types.md)). 

When released, SMD-funded software should follow best practices in the relevant open source and research communities.  For example, providing documentation and testing, which are not required to be provided under SPD-41a, alongside the source code increases the quality of the software and reusability of the software. 

For publicly available software projects, SMD-funded software projects must include a code of conduct and guidelines for how to make contributions.  A code of conduct provides clear guidelines for the conduct of those participating in the development of the software.  The guidelines for how to make contributions provide clear expectations for how to contribute to the project.  This may include how to make contributions, the type of contributions that the project is accepting, or even that the project is currently not accepting contributions.  This can also include the expectations for support for the software project and for responding to questions about the project.  

When released as open source software, source code for SMD-funded software shall be made available in a publicly accessible repository that is widely recognized by the community.  See the section on ‘Where to Share Software’ for more information and examples of how to make the software available.  

Publicly available SMD-funded software must be citable using a persistent identifier. A persistent identifier such as a DOI provides an easy method for software to be cited in the scientific literature and for the developers of the software to receive credit for their work. It also provides a way to track the usage of the software and to make reporting on the software easy. 

For software developed under research grants, there is no expectation that the software is maintained.  Some scientific software is developed for a single purpose, and there is no benefit in further development or maintenance of the software.  Providing it openly does help to further the understandability of the scientific work that it supports as a manuscript may not capture all of the details in the processing or analysis required to reproduce the results. 

## Reporting Open-Source Software
Publicly available SMD-funded software shall be indexed as part of the NASA catalog of software. Developers of software packages that are developed as part of SMD-funded activities must catalog the software in in NASA’s [New Technology Reporting System](https://invention.nasa.gov/). Single use software and commercial software do not need to be reported for indexing as part of the NASA catalog of software.

## Intellectual Property and Licenses for Software
If there are no other restrictions, publicly available SMD-funded software should be released under a permissive license that has broad acceptance in the community. Restrictions that may prevent release under a permissive license include, but are not limited by, software governed by incompatible licenses or inclusion of restricted computer software. Seek specific advice from the Chief Science Data Office or Intellectual Property Counsel, as needed. Questions can be submitted to HQ-SMD-SPD41@list.nasa.gov. 

For software developed at NASA Centers and released through the NPR 2210 process, Center Intellectual Property Counsel shall be consulted in the selection of the license to be used in the release of software, which may include Apache 2.0, BSD, or MIT.

