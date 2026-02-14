---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Education

* **Ph.D. in Computer Science and Technology**, Fudan University, Shanghai, China (September 2022 - June 2027, expected)
* **B.S. in Cybersecurity**, Sichuan University, Chengdu, China (September 2018 - June 2022)

## Research Projects

### Vulnerability Knowledge Base Quality Enhancement Tools
Research on open-source vulnerability quality enhancement techniques based on multi-source knowledge and static analysis, constructing a high-trust and explainable vertical domain knowledge base to address hallucination and data timeliness issues in large language models' application to software supply chain security.

* **Multi-dimensional Knowledge-based Affected Component Identification Tool** (Core Contributor | ICSE'24 (CCF-A) First Author)
  * Addressing the problem of missing or inaccurate affected component information in open-source vulnerabilities, we integrate multi-source vulnerability knowledge from NVD, GitHub Advisory, etc., and design an automatic identification method for affected components based on multi-dimensional knowledge association and cross-ecosystem mapping. This has enhanced the coverage and accuracy of component attribution information for over 200 vulnerability entries in CVE, GitHub, and GitLab vulnerability knowledge bases.

* **Static Analysis-based Affected Component Version Identification Tool** (Core Contributor | ASE'24 (CCF-A) First Author & TOSEM'26 (CCF-A) First Author, Major Revision)
  * Addressing the problem of coarse-grained and imprecise vulnerability-affected version range annotations, we combine patch code static analysis with version evolution tracking technology to achieve fine-grained automatic identification of affected component versions. This has enhanced version information for over 300 Java and C/C++ vulnerability entries in CVE, GitHub, and GitLab vulnerability knowledge bases, providing precise version-level vulnerability matching capabilities for Software Composition Analysis (SCA).

* **Semantic-enhanced Critical Change Identification Tool for Vulnerability Patches** (Core Contributor | TOSEM'26 (CCF-A) First Author, Major Revision)
  * Addressing the problem of vulnerability patches containing numerous non-security-related changes that hinder downstream analysis, we propose a semantic-enhanced automatic identification method for critical patch changes, accurately extracting core code changes directly related to vulnerability fixes from complex patches, effectively improving the efficiency and accuracy of downstream vertical domain analysis tasks such as vulnerability detection and patch migration based on large models.

### LLM-based Vulnerability Detection and Test Case Generation Tools
Research on vulnerability detection and test case generation techniques that integrate large language models with static analysis, covering source code vulnerability detection, recurring vulnerability detection, and automatic vulnerability PoC generation, improving the efficiency and accuracy of vulnerability discovery and verification.

* **Semantic Weaving-based LLM Vulnerability Detection Tool (VulWeaver)** (Core Contributor | Huawei Internal Network Security Laboratory)
  * Addressing problems in existing source code vulnerability detection methods where static analysis constructs imprecise program representations, extracts incomplete vulnerability contexts, and has opaque large model reasoning, we propose a semantic weaving-based vulnerability detection method VulWeaver. By integrating deterministic rules with large model semantic reasoning to construct an enhanced unified dependency graph, combining program slicing to extract complete vulnerability contexts, and adopting a meta-prompting framework to drive expert-level reasoning based on vulnerability types. Achieved F1 score of 0.75 on CrossVul dataset, improving 14%-53% over the best baseline; discovered 26 vulnerabilities in 9 real Java projects, with 15 confirmed by developers and 5 receiving CVE numbers.

* **Static Analysis-based Recurring Vulnerability Detection Tool (AntMan)** (Core Contributor | Huawei Huyanglin Project | ISSTA'25 (CCF-A) Second Author)
  * Addressing the problem of existing methods performing poorly on diverse variant types in recurring vulnerability detection caused by code reuse, we constructed a large-scale benchmark dataset containing 4,569 recurring vulnerabilities (expanding 953% compared to existing datasets), systematically evaluated the limitations of existing methods, and proposed AntMan, a fine-grained vulnerability signature generation method based on inter-procedural taint analysis and intra-procedural dependency slicing, combined with flexible graph matching strategies to achieve high-precision recurring vulnerability detection. Achieved precision of 0.84 and recall of 0.85, successfully detected 4,593 recurring vulnerabilities (307 confirmed by developers), discovered 73 0-day vulnerabilities, with 5 receiving CVE numbers.

* **Option-aware Directed Greybox Fuzzing Tool for Vulnerability PoC Generation (CoupleFuzz)** (Core Contributor | FSE'26 (CCF-A) First Author, Major Revision)
  * Addressing the problem of potential vulnerabilities discovered by static analysis tools lacking reproducible PoC verification, we propose CoupleFuzz, an option-aware directed greybox fuzzing tool that redefines PoC input as a combination of option input and file input. Through static analysis to extract option knowledge and dynamic inference of option validity, adopting a cross-guided strategy to coordinate option mutation and file mutation, significantly improving the efficiency and reachability of vulnerability PoC generation. Generated 15 more PoCs than the best directed greybox fuzzing baseline (3.1x improvement), with target location reach speed averaging 5.6x acceleration, discovered 6 0-day vulnerabilities confirmed by developers, with 1 receiving a CVE number.

### Semantic and Syntactic-Enhanced LLM Automated Vulnerability Patch Migration Tools
Addressing the problem that vulnerability patches in open-source software multi-branch management cannot be directly migrated due to code differences between branches, and existing methods have deficiencies in vulnerability semantic understanding and code structure parsing, we propose Mystique, a semantic and syntactic-enhanced LLM automated vulnerability patch migration method, achieving precise vulnerability patch migration. It has been integrated into Huawei OpenEuler community and deployed at the Institute of Software, Chinese Academy of Sciences.

* **Semantic and Syntactic-Enhanced LLM Automated Vulnerability Patch Migration Tool (Mystique)** (Core Contributor | Institute of Software, CAS | Huawei OpenEuler | FSE'25 (CCF-A) First Author, ACM SIGSOFT Distinguished Paper Award | CCF Software Prototype Competition 2nd Prize, First Contributor)
  * Addressing the shortcomings of existing patch migration methods that ignore vulnerability-related semantic context or introduce irrelevant code, we propose extracting original fix functions and target vulnerability function signatures through vulnerability semantic slicing and syntactic correctness guarantees, combined with fine-tuned large language models to generate fix functions and ensure migration quality through iterative verification and refinement. Achieved patch migration success rates of 95.4% at function level and 92.4% at CVE level, improving at least 13.2% and 12.3% respectively compared to existing best methods, successfully completing patch migration for 34 real-world vulnerability branches. The open-source version of Mystique has been integrated into Huawei OpenEuler community, reducing manual costs by 90% while improving the community's vulnerability patch migration success rate by 10%, and received a community thank-you letter; Mystique and its toolchain have also been deployed at the Institute of Software, Chinese Academy of Sciences.

### Large Model Supply Chain Quality Assurance Methods
Research on risk measurement and dependency recovery technologies for open-source large model supply chains, covering systematic analysis of large model supply chains from usage, evolution, quality, and risk perspectives, as well as automated recovery of model dependency relationships, providing fundamental technical support for secure and trustworthy governance of large model supply chains.

* **Systematic Risk Analysis of Open-source Large Model Supply Chains** (Core Contributor | ICSE'26 (CCF-A) Corresponding Author)
  * Constructed the first large-scale model supply chain based on Hugging Face (covering 1.82 million models and 540,000 dependency relationships), conducted the first systematic empirical study from four dimensions: usage, evolution, quality, and risk. Found that 31% of models have dependency relationships but contribute 88% of downloads, 83% of models lack performance metrics, and different transformation operations such as fine-tuning, quantization, and merging have differentiated propagation effects on risks such as hallucination, jailbreaking, and prompt injection, providing actionable governance recommendations for various stakeholders in the model supply chain.

* **Model Dependency Recovery Tool for Large Model Supply Chains** (Core Contributor | Ministry of Science and Technology 2030 Major Project | ISSTA'26 (CCF-A) First Author, Under Review)
  * Through connectivity-based model clustering to handle open dependency topologies, and adopting a divide-and-conquer strategy using type-specific fingerprints to achieve precise identification of three dependency types: quantization, merging, and fine-tuning. Constructed the first benchmark dataset MDGBench covering 137 real models and 131 dependency edges. Achieved ARI of 0.96 on clustering tasks (39% improvement over best baseline), dependency identification DF₁ of 0.82 (193% improvement over best baseline). Applied to 289 isolated models, successfully recovered 189 missing dependency relationships, with 42 confirmed by model authors.

### Vulnerability Membership Inference Tools for Large Models
Research on vulnerability code membership inference technology for code large language models, by integrating static analysis with model internal probabilities and output representations, determining whether specific vulnerability code belongs to model training data, providing technical support for security traceability and risk governance of code generated by large models.

* **Fusion Feature-based Vulnerability Code Membership Inference Tool (VulInception)** (Core Contributor | USENIX Security'26 (CCF-A) First Author, Under Review)
  * Addressing the problem that existing code membership inference methods have difficulty distinguishing vulnerability code from its fixed versions, we propose VulInception, a fusion feature-based vulnerability code membership inference method. By constructing abstract syntax trees and performing fine-grained program slicing based on data and control dependencies, accurately locating vulnerability-related code nodes; designing Local Determinism-Residual Document Frequency (LD-RDF) metrics to quantify the triviality of code tokens, calibrating model output probabilities to filter non-memorization signals; adopting a statement-level iterative code completion strategy to alleviate the semantic forgetting problem of one-time completion; finally fusing calibrated probability representations with code graph representations, achieving precise discrimination between vulnerability code members and non-members through a dual-branch self-attention classifier.

### Software Supply Chain Security Risk Governance

* **Fuxi: Software Supply Chain Risk Governance Platform** (Core Contributor | Fudan University Software Engineering Laboratory Self-developed Risk Governance Platform)
  * Functions include: open-source software security vulnerability analysis, open-source vulnerability reachability analysis, software version upgrade recommendations. Built databases: 9.13 million Java version repositories, 12 million Go version repositories, 3 million Python version repositories, 100 million JavaScript version repositories, 190,000 CVE data entries. To date, discovered 333 malicious packages in PyPI ecosystem and 208 malicious packages in NPM ecosystem. Related achievements have been successfully applied in cooperative projects with enterprises such as **Huawei**.

## Publications

  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
## Talks

  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
## Awards and Academic Service

### Research Achievements

* **Vulnerability Knowledge Base Enhancement**: Enhanced component knowledge for 214 CVEs; improved version range accuracy for 309 CVEs
* **LLM-based Vulnerability Discovery**: Discovered 187 0-day vulnerabilities; 23 received CVE IDs
* **LLM-based Automated Program Repair**: ACM SIGSOFT Distinguished Paper Award; CCF Software Prototype Competition 2nd Prize; Successfully merged patches for 34 0-day vulnerability project branches
* **Open-source Large Model Ecosystem Governance**: Recovered 189 missing dependency relationships for large models; 43 dependency-missing models are in the top 1,000 by Hugging Face downloads

### Academic Reports

* 2024 CCF Open Source Ecosystem and Software Supply Chain Workshop
* 2025 CCF Software Conference - Open Source Supply Chain Security Analysis Frontier Research Forum

### Scholarships

* National Scholarship × 1
* Tencent Scholarship × 1
* Huawei Named Scholarship × 1
* Dong Named Scholarship × 1
* University-level Scholarships × 3

## Skills

### Programming Languages
Java, Python, C/C++, Bash, LaTeX

### Program Analysis Development Tools
Tree-Sitter, Joern, Soot, SVF, Git

### Deep Learning Development Tools
PyTorch, TensorFlow, vLLM

### Foreign Languages
CET-4, CET-6
