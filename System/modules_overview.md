# Modules & Tools Overview

This page contains modules that the BEXIS2 community has developed. They are provided "as is" without any warranty or liability. Please use at your own risk.

Most of the modules are constantly under development and are not (yet) provided as releases that match the official BEXIS2 releases. We hope to get there in the future. For the time being, if you are interested in using a module please contact the individual provider and to learn about the current status and how to use the module.


| Name | Description | Status | Type | Contact |
| :-- | :-- | :-- | :-- | :-- |
 | AD Annotation Module (AAM)[New Module] | provides a semantic annotation tool on the fly over the variables using the AD Ontology to be used by the semantic search | Intern | Module | AquaDiva Team | 
 | Analysis and Statistics Module (ASM) | Provides a Global Graph overview of the semantic meanings of the selected dataset - Graphical representation of the Numerical/categorical attributes of the primary data - provides a global report about the data portal (semantic coverage, numerical coverage, dataset, and variable coverage) | Intern | Module | AquaDiva Team | 
 | BEXIS2-VAT System Interface (BEXIS2-VAT) | This BEXIS2 module extends the system with an interface to the Geo Engine | BEXIS2 | Module | BEXIS2 | 
 | Digital Object Identifier (DOI) Assignment Workflow (DOIAW) | A module that allows datasets to be linked to DataCite DOI metadata and to send DOI requests to a DOI proxy. | Under development | Module | BEXIS2 / BExIS team | 
 | Event Management (EMM) | Simple to customize tool to manage participants registration for events (e.g., workshops, meetings, ...). Based on a fully flexible registration form. No user account is needed for registration. Update your registration before the deadline.  | Public | Module | BExIS team | 
 | File Management (FMT) | Tool to upload and remove files. It is customizable and system-wide usable. Manage your (non-dataset) files in a topic-centered manner. | Public | Module | BExIS team | 
 | Land-use Intensity (LUI) | A tool to calculate the index of land-use intensity (LUI) according to Blüthgen et al. (2012), based on information from the land owners on mowing, grazing and fertilization (Vogt et al. 2019) and your selections via a user-friendly interface. https://www.bexis.uni-jena.de/LUI/LUICalculation/DownloadPDF?fileName=LUI-citation.pdf | Public | Module | BExIS team | 
 | Omic Archives (OAC) | Import/retrieve Succession Metadata (and its sequence samples) from Sequence data portal (EBI, BioGps, NCBI) into the portal as primary data   | Intern | Module | AquaDiva Team | 
 | Open Archives Initiative Protocol for Metadata Harvesting  (OAIPMH) | This module extends a BEXIS2 instance with the functionality that BEXIS2 works as a data provider for all harvesters according to the OAI-PMH (Open Archives Initiative Protocol for Metadata Harvesting) protocol. | Public | Module | BEXIS2 team | 
 | Photo Gallery (PGM) | Customized system to manage photos. You can easily preview, filter, and pick photos for later ordering. | Intern | Module | BExIS team | 
 | Plot profiling tool | A tool to count the number of plot IDs from a list or a file. The plots will also be categorized. | Intern | Module | BExIS team | 
 | Publication Management (PUB) | Module to manage publications.  | Public - depreciation candidate | Module | BExIS team | 
 | Resource Booking (RBM) |  Resource booking management module: This is a calendar-based tool for managing any resource. It is highly configurable to cover multiple scenarios. It helps communicate the bookings and activities to all users (colleagues and other stakeholders). | Public | Module | BExIS team | 
 | Sample Archive (RDB) |  | Intern | Module | MPI / BEXIS2 team | 
 | Static Websites (SWS) | Module to integrate static websites into BEXIS2. Customizable and system-wide usable. | Intern | Module | BExIS team | 
 | Synthesis Proposal Module (SPM) | A module that provides a workflow to announce synthesis proposals. A synthesis proposal is a project-specific document describing a research thesis that requires multiple datasets. | Planned | Module | BExIS team | 
 | Unstructured Data Analysis Module (UDAM)[New Module] | provides an analysis tool for the .fastq and .fq files from sequence data groups to analyze raw data online -Will be deleted due to a large amount of storage needed for the sequence raw data files (.fq and .fastq ) | Intern | Module | AquaDiva Team | 
 | Former Member Management (ALM) |  | Public | Module integrated in BEXIS2 | BExIS team | 
 | Multimedia Management (MMM) |  | Part of BEXIS2 | Module integrated in BEXIS2 | iDiv / BEXIS2 team | 
 | Digital Object Identifier (DOI) proxy | A proxy server to  communicate between a BEXIS2 application and a DataCite DOI server. It helps to assign DOIs to datasets. | Under development | Proxy server | contact? | 
 | Changed datasets notification | App that regularly informs BEXIS2 users about datasets that have been changed. | Intern | Standalone application | BExIS team | 
 | Curation notification | App that automatically creates GitHub issues for the newly created datasets to support the  curation process. Based on the GitHub issue and a workflow defined by us, reminder emails with a list of required or recommended adjustments for the data set are sent to the user. | Under development | Standalone application | BExIS team | 
 | New datasets notification | App that regularly informs all BEXIS2 users about all newly created datasets. | Intern | Standalone application | BExIS team | 
 | Open request notification | App that checks whether requests have been unanswered for longer than a defined number of days and then automatically sends a reminder to the user. | Intern | Standalone application | BExIS team | 
 | Interactive Search (IS) | Graphical Map search based on Well locations (Will be deleted since the locations are introduced into the AD metadata and can be used as a search attribute) | Intern | Feature | AquaDiva Team | 
 | Metadata Migration and Metadata Mapping (4M)  | Using the UI from Bexis to map the system variable to implement metadata nodes and migrate from a metadata schema to another using this graphical mapping - bulk migration feature | Intern | Feature | AquaDiva Team | 
 | Previous Metadata Schema Load (4M) | Include the view to load previous metadata versions in case of changed metadata schema | Intern | Feature | AquaDiva Team | 
 | Search Attributes (SA) | Include the search attribute facet data type to handle UI elements: dates -> date picker, numeric -> range and sliders, string -> selection (in progress) | Intern | Feature | AquaDiva Team | 
 | Search Attributes Primary data Nodes (SA)[DDM feature] | Make search attributes also connect to the variables through the Semantic layer and annotations used over the data attributes/variables - Note: the unit issue is still in progress to handle conversions between primary data | Intern | Feature | AquaDiva Team | 
 | Semantic Search (SS)[DDM feature] | provides a semantic search over the search query using the semantic Layer from AD Ontology and Annotations | Intern | Feature | AquaDiva Team | 
 | Citation tool | A tool to provide a citation string for one or more datasets based on dataset IDs. Supported citation formats are BibTex, RIS, and text. | Intern | Module with API | BExIS team | 
 | Citation widget | A widget that can be integrated into the dataset landing page to provide the citation string for this specific dataset. Supported citation formats are BibTex, RIS, and text. | Intern | Widget | BExIS team | 
 | Analysis Server (SS) | Flask python server providing categorical - numerical - semantic analysis using standard analysis algorithms and An A.I network for semantic analysis | Intern | API | AquaDiva Team | 
 | Semantic Search (SS) | Java Spring EndPoints providing NLP analysis: Extract Entities and characteristics from a Search sentence - provides Ontology and semantic queries over the KB of AD annotations and ontology | Intern | API | AquaDiva Team | 
 | Semedico (Semedico) | Flask python server providing semantic search over publication (AD cluster, Semdev) using the semantic layer of AD Ontology | Intern | API | AquaDiva Team | 

