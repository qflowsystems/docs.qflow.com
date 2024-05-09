---
layout: default
title: Document Classifications
nav_order: 2
parent: Working with Documents
has_toc: false
---
# Document Classifications
---
In QAction, documents are organized by classifications. When a document is added, the user must select its classification. The classification is stored as an index value for the document.

A document’s classification determines its:
* Default Security – the users who can view or modify the document or its indexes.
* Index Fields – the data fields that are entered when a document is added.
* Document Types – the list of document types selected when storing the document.
    
Document classifications are represented as a hierarchy. Each document must be filed under a classification. The classification associated with a specific document is shown as a path from the top level of the hierarchy (ex. Internal/Financial/Annual Reports).

Within a classification hierarchy, there are Entity entries (company or organization) or Person entries (employee, contact). When the classification hierarchy is maintained by an administrator, the generic term ‘Entity’ or ‘Person’ is used. When a document is stored, the specific entity (ex. IBM) or person (ex. David Johnson) must be selected. The system stores full demographic information for entities and persons. This information can be referenced when viewing documents for those entities or persons.

Each classification has specific document types that can be assigned to documents. In the sample classification hierarchy mentioned previously, document types are only shown for the Internal/HR/Personnel File/{Person} classification.

An application administrator maintains the document classification hierarchy. They can add, modify, or deactivate classifications.