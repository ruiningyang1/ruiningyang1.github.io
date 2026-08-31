---
layout: paper
title: "Measuring Security Hardening Adoption in Infrastructure as Code: An Empirical Study of Public Repositories"
authors_display: "Ruining Yang, Nick Nikiforakis"
citation_authors:
  - "Yang, Ruining"
  - "Nikiforakis, Nick"
citation_date: "2026/08/26"
citation_conference: "23rd Annual International Conference on Privacy, Security and Trust (PST)"
citation_publisher: "IEEE"
venue: "23rd Annual International Conference on Privacy, Security and Trust (PST), Ottawa, Canada, 2026"
status: "Presented August 2026. IEEE Xplore listing expected around December 2026."
# Author's accepted version, not the PDF from IEEE Xplore.
pdf: /publication/2026_pst_measuring.pdf
# citation_doi: 10.1109/...                 # fill in once the paper is in IEEE Xplore
rights: "&copy; 2026 IEEE. Personal use of this material is permitted. Permission from IEEE must be obtained for all other uses, in any current or future media, including reprinting/republishing this material for advertising or promotional purposes, creating new collective works, for resale or redistribution to servers or lists, or reuse of any copyrighted component of this work in other works."
bibtex: |
  @inproceedings{yang2026measuring,
    title={Measuring Security Hardening Adoption in Infrastructure as Code: An Empirical Study of Public Repositories},
    author={Yang, Ruining and Nikiforakis, Nick},
    booktitle={Proceedings of the 23rd Annual International Conference on Privacy, Security and Trust (PST)},
    year={2026},
    organization={IEEE}
  }
---

## Abstract

Security hardening is a critical practice for managing server infrastructure. Yet, despite the availability of many guides on how to harden servers, the actual adoption of these hardening steps is unknown. Infrastructure as Code (IaC) automates the setup, configuration, and management of servers in a reproducible and auditable way. In modern environments, IaC is the ideal medium through which to harden newly-provisioned servers since it would guarantee the consistent security hardening of all servers simultaneously.

In this paper, we systematically collect and analyze the hardening guidance from 50 public security guides, translating it into IaC steps. Inspired by the term of "security smells" in software engineering, we refer to the absence of security-hardening steps as "ghost smells", i.e., steps that should be there yet are absent. Using Large Language Models, we analyze millions of public IaC playbooks across hundreds of thousands of GitHub repositories, to quantify the actual adoption of security hardening.

Overall we find minimal adoption of what are considered critical steps in hardening a new server. Approximately 10% of the repositories written in one of the most popular IaC languages take any hardening steps, with most IaC focusing primarily on securing Linux but largely ignoring the hardening of common server software. Our results indicate that ghost smells are a real issue in IaC and warrant inclusion in static analysis tools.
