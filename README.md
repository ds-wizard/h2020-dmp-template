# H2020 DMP

The template is based on the official [Template Horizon 2020 Data Management Plan (DMP) v2.0](https://ec.europa.eu/research/participants/data/ref/h2020/other/gm/reporting/h2020-tpl-oa-data-mgt-plan-annotated_en.pdf) designed for use in [Data Stewardship Wizard](https://ds-wizard.org) with [*Common Data Stewardship knowledge model*](https://registry.ds-wizard.org/knowledge-models/dsw:root:latest) and [*Life Sciences DSW Knowledge Model*](https://registry.ds-wizard.org/knowledge-models/dsw:lifesciences:latest).


## Usage

This template is available through [DSW Registry](https://registry.ds-wizard.org/templates).


## Issues and Contributing

This document template for DSW is available as open-source via GitHub Repository [ds-wizard/h2020-dmp-template](https://github.com/ds-wizard/h2020-dmp-template), you can [report issues](https://github.com/ds-wizard/h2020-dmp-template/issues) there and fork it for customizations or contributions.


### Contributors

* **Marek Suchánek** <[marek.suchanek@ds-wizard.org](mailto:marek.suchanek@ds-wizard.org)>
  * ORCID: [0000-0001-7525-9218](https://orcid.org/0000-0001-7525-9218)
  * GitHub: [@MarekSuchanek](https://github.com/MarekSuchanek)
* **Kryštof Komanec** <[krystof.komanec@ds-wizard.org](mailto:krystof.komanec@ds-wizard.org)>
  * ORCID: [0000-0003-3856-1682](https://orcid.org/0000-0003-3856-1682)
  * GitHub: [@krystofkomanec](https://github.com/krystofkomanec)
* **Jana Martínková** <[jana.martinkova@ds-wizard.org](mailto:jana.martinkova@ds-wizard.org)>
  * ORCID: [0000-0001-8575-6533](https://orcid.org/0000-0001-8575-6533/)
  * GitHub: [@jmartinkova](https://github.com/jmartinkova)

Starting v1.28.0, AI tools (Codex, Claude Code) are used to assist in the development of this template. The AI tools are used to generate text, fix typos, and improve grammar. The AI tools are used to assist the human contributors in the development of the template.

## Changelog

### 3.0.0

- Replies are read by the annotations of the knowledge model (`json.key`, `json.value`) instead of UUIDs; requires the Common DSW Knowledge Model (`dsw.root`) or the Life Sciences DSW Knowledge Model (`dsw.lifesciences`) 2.8.1 or newer
- The data model is separated from rendering: `src/data/model.j2` extracts the replies (`extract_replies` version 2, which includes unanswered questions) and maps them, the other templates only render
- Adjusted to the knowledge model 2.8: metadata and provenance standards from FAIRsharing (section 2.1), provenance kept by a workflow system (section 2.1), the grant number of the funding selected for a cost (section 3)
- Fixed "Roles" shown for contributors with a single role
- Fixed the instructions to get access to open metadata (the answers were swapped) and the conditions of use of re-used non-reference datasets that were never shown (section 2.2)

### 2.0.0

- Adjusted to Wizard 5.0 (template metamodel version 19.0, template id `dsw.h2020-dmp`, knowledge models `dsw.root` and `dsw.lifesciences`)
- Translated documents declare their language (`lang`), show dates with translated month names, and translate "N/A"
- Fixed the information table on the front page covering the title when there are many contact people or creators

### 1.28.0

- Support for template localization (Wizard 4.35+, metamodel 18.3), with a Czech test translation in `locales/cs.po`
- Fixed sections that were never rendered because of missing or wrong UUIDs and paths: access control of a shared working space, metadata standards, archiving in cold storage after the project, and the current version on the front page
- Fixed projects requiring ethical approval listed once per authority (and not at all without one)
- Fixed the HTML structure (block elements inside paragraphs, unclosed and stray tags, empty paragraphs and lists, text mixed with blocks in containers)
- Fixed the "Data Management Plan" title on the front page missing in the LaTeX and OpenDocument formats
- Fixed answers about the utility of datasets for other fields being lowercased
- Fixed typos and grammar

### 1.27.1

- Fixed text value type questions rendering with markdown

### 1.27.0

- Adjust to template metamodel version 18.0 (released in DSW 4.29.0)

### 1.26.1

- Adjust to template metamodel version 17.1 (released in DSW 4.26.0)

### 1.26.0

- Updated reused dataset name to use reply string value instead FAIRsharing integration
- Updated dependency on KM to 2.7.0
- Improved qualified references part
- Fixed rendering risks
- Fixed rendering reused datasets conditions
- Fixed the published dataset to reflect future-oriented statement

### 1.25.0

- Fixed non-equipment datasets utility
- Improved text

### 1.24.0

- Updated dependency on KM to 2.6.13
- Fixed legacy integration type

### 1.23.0

- Updated integrations to metamodel version 17.0 (released in DSW 4.22.0)

### 1.22.0

- Adjusted to template metamodel version 17.0 (released in DSW 4.22.0)
- Fixed typos

### 1.21.0

- Added "General-purpose repository" option to repository type descriptions

### 1.20.0

- Added ORCID Integration
- Added compatible knowledge models to README

### 1.19.0

- Improved Authors of the DMP

### 1.18.0

- Adjusted to template metamodel version 16 (released in DSW 4.13.0)

### 1.17.0

- Adjusted to template metamodel version 15 (released in DSW 4.12.0)

### 1.16.0

- Adjusted to template metamodel version 14 (released in DSW 4.10.0)

### 1.15.1

- Fixed nested bullet points would display unwanted characters

### 1.15.0

- Fixed Questions 2 (part 1) regarding data versions to allow for multiple choices
- Improved Question 2 (part 4) regarding access to private data and reasons destroying data
- Improved Question 3 regarding costs in project

### 1.14.0

- Adjusted to template metamodel version 13 (released in DSW 4.3.0)

### 1.13.1

- Fixed broken images in Word

### 1.13.0

- Adjusted to template metamodel version 11 (released in DSW 3.20.0)

### 1.12.2

- Removed unused uuids

### 1.12.1

- Fixed extra `endif`

### 1.12.0

- Updated for `dsw:root:2.5.0`

### 1.11.0

- Switched from `wkhtmltopdf` to `weasyprint` for PDF
- Improved styling for PDF and HTML
- Fixed (non-)reference data in data summary
- Aligned data openness with the KM
- Fixed privacy use / cannot use issue

### 1.10.0

- Added versions overview / change tracker table
- Adjusted to template metamodel version 11 (released in DSW 3.20.0)

### 1.9.1

- Fixed use of "Describe your SOP (Standard Operating Procedure) for file naming" (`9ff389f0-2236-48cf-880c-040ea1bb0d2f`)

### 1.9.0

- Adjusted to template metamodel version 10 (released in DSW 3.12.0)

### 1.8.0

- Adjusted to template metamodel version 9 (released in DSW 3.10.0)

### 1.7.1

- Fixed Jinja template nesting error

### 1.7.0

- Compatible with `dsw:root:2.4.0`

### 1.6.0

- Adjusted to template metamodel version 8 (released in DSW 3.8.0)

### 1.5.0

- Adjusted to template metamodel version 7 (released in DSW 3.7.0)

### 1.4.0

- Adjusted to template metamodel version 6 (released in DSW 3.6.0)
- Started to use the new document context where suitable

### 1.3.0

- Adjusted to template metamodel version 5 (released in DSW 3.5.0)
- Fixed of typo "provice" in section 2.1

### 1.2.0

- Adjusted to template metamodel version 4 (released in DSW 3.2.0)

### 1.1.1

- Fixed displaying answers related to measured datasets

### 1.1.0

- Adjusted to template metamodel version 3 (released in DSW 2.12.0)

### 1.0.0

Initial version developed during the [BioHackathon Europe 2020](https://www.biohackathon-europe.org).
