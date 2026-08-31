---
layout: paper
title: "Infrastructure as Compromise: Abusing Residual Trust in Infrastructure as Code Tools"
authors_display: "Ruining Yang, Narong Chaiwut, Nick Nikiforakis"
citation_authors:
  - "Yang, Ruining"
  - "Chaiwut, Narong"
  - "Nikiforakis, Nick"
citation_date: "2026/06/23"
citation_conference: "Proceedings of the Sixteenth ACM Conference on Data and Application Security and Privacy (CODASPY '26)"
citation_publisher: "ACM"
citation_firstpage: "126"
citation_lastpage: "137"
citation_doi: "10.1145/3800506.3803500"
venue: "16th ACM Conference on Data and Application Security and Privacy (CODASPY), Frankfurt am Main, Germany, 2026"
pdf: /publication/2026_codaspy_infrastructure.pdf
rights: "Published under a Creative Commons Attribution 4.0 International License."
bibtex: |
  @inproceedings{yang2026infrastructure,
    title={Infrastructure as Compromise: Abusing Residual Trust in Infrastructure as Code Tools},
    author={Yang, Ruining and Chaiwut, Narong and Nikiforakis, Nick},
    booktitle={Proceedings of the Sixteenth ACM Conference on Data and Application Security and Privacy},
    pages={126--137},
    year={2026},
    doi={10.1145/3800506.3803500}
  }
---

## Abstract

Infrastructure as Code (IaC) has transformed the way developers deploy and manage their infrastructure, enabling automated, reproducible, and version-controlled builds. At the same time, developer errors in IaC configurations can result in thousands of identically-vulnerable servers.

In this paper, we study the so-far ignored problem of residual trust in IaC tools. IaC configurations (also known as playbooks) can refer to remote code and data that will be fetched upon execution and be incorporated in the resulting infrastructure. As such, attackers can perform supply-chain attacks against IaC environments by taking over the third-party resources that are used by playbooks during the build process. To understand the attack surface of this threat, we focus on Ansible and Puppet and quantify all the ways that developers can introduce remote references in their code. We then perform a large-scale study of publicly-available IaC playbooks on GitHub to characterize the ways through which developers actually introduce remote references in their IaC scripts. By analyzing IaC playbooks in 247,131 repos, we identify 463 expired domains that can be immediately registered by attackers and 10,400 instances of misconfigurations in the addressed remote hosts. Our analysis also identified evidence of typosquatting errors across 30 Ansible repositories and 16 Puppet repositories, as well as a novel attack vector involving placeholder domain names. In recognition of the magnitude of the identified problems, we propose DependoScope, an extension for a popular code editor that steers developers away from erroneous remote references.
