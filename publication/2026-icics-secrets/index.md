---
layout: paper
title: "When Secrets Get Committed: The Role of Code Platforms in Avoiding Secret Leakage"
authors_display: "Ruining Yang, Billy Tsouvalas, Nick Nikiforakis"
citation_authors:
  - "Yang, Ruining"
  - "Tsouvalas, Billy"
  - "Nikiforakis, Nick"
citation_date: "2026/10/27"
citation_conference: "28th International Conference on Information and Communications Security (ICICS)"
citation_publisher: "Springer"
citation_firstpage: "259"
citation_lastpage: "279"
venue: "28th International Conference on Information and Communications Security (ICICS), Fukui, Japan, 2026"
# Author's accepted version, not the PDF from SpringerLink.
pdf: /publication/2026_icics_secrets.pdf
rights: "This is the authors' accepted manuscript. The final authenticated version is available on SpringerLink."
bibtex: |
  @inproceedings{yang2026secrets,
    title={When Secrets Get Committed: The Role of Code Platforms in Avoiding Secret Leakage},
    author={Yang, Ruining and Tsouvalas, Billy and Nikiforakis, Nick},
    booktitle={Proceedings of the 28th International Conference on Information and Communications Security (ICICS)},
    pages={259--279},
    year={2026},
    publisher={Springer}
  }
---

## Abstract

Secret leakage refers to accidentally including sensitive tokens (such as API keys) in public software artifacts. Specific to code platforms (such as GitHub and GitLab), prior work has shown that developers commonly expose secrets in their open-source software, allowing fast-acting attackers to abuse them in order to steal data and resources.

In this paper, we seek to understand the role of code platforms on curbing secret leakage, through a two-pronged analysis. First, we evaluate the ability of ten popular code platforms to detect and prevent secret leakage at the time of code publication. Next to detecting plaintext secrets, we also quantify whether these platforms are able to detect other popular secret formats, such as, Base64-encoded secrets and concatenated secrets. By deploying 300 repositories with real secrets, we find that just 20% of the evaluated platforms perform any type of secret detection, significantly underperforming popular secrets scanners.

Second, using the same controlled repositories, we perform an in-the-wild analysis of malicious scanners. Namely, over a period of one month, we observed 2,126 matched credential use attempts from 553 unique IP addresses, abusing secrets from 34 of our repositories.

Overall, our results highlight that hundreds of malicious bots are lying in wait looking for secrets that get accidentally published in open-source software. These results show that there is a real need, not just for better developer education, but also for the platforms themselves to engage in proactive detection of leaked secrets, before attackers do.
