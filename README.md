# University of Otago (university-of-otago)

The University of Otago is New Zealand's oldest university, founded in 1869 in Dunedin, and ranked #214 in the QS World University Rankings 2025. This repository catalogs the institution's public developer and API footprint as an [APIs.json](https://apisjson.org) provider profile. Otago has no dedicated public developer portal or documented public API program; its concrete machine interfaces are infrastructure-oriented — an OUR Archive (Esploro) OAI-PMH research-metadata endpoint and Tuakiri federated (SAML 2.0 / Shibboleth) single sign-on.

- APIs.json: https://raw.githubusercontent.com/api-evangelist/university-of-otago/refs/heads/main/apis.yml
- Run with Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=university-of-otago-api-evangelist&utm_content=repo

## Type

- Index
- Consumer
- 3rd-Party

## Tags

Education, Higher Education, University, Research, Open Access, Repository, Identity, New Zealand

## APIs

- **OUR Archive OAI-PMH Metadata** — Standards-based OAI-PMH metadata endpoint for the Otago University Research Archive (Ex Libris / Clarivate Esploro). Resolves and returns valid OAI XML but currently responds with error_code 21 (public harvesting not enabled). Docs: https://developers.exlibrisgroup.com/esploro/integrations/oai/ — Repository: https://ourarchive.otago.ac.nz/
- **Tuakiri Federated Identity (SAML 2.0 / Shibboleth)** — University SAML/Shibboleth Identity Provider within the Tuakiri NZ Access Federation (REANNZ) for federated single sign-on. Federation infrastructure rather than a self-service API. Docs: https://docs.tuakiri.ac.nz/

## Plans

- [plans/university-of-otago-plans-pricing.yml](plans/university-of-otago-plans-pricing.yml)

## Rate Limits

- [rate-limits/university-of-otago-rate-limits.yml](rate-limits/university-of-otago-rate-limits.yml)

## FinOps

- [finops/university-of-otago-finops.yml](finops/university-of-otago-finops.yml)

## Timestamps

- Created: 2026-06-03
- Modified: 2026-06-03

## Common Properties

- Website: https://www.otago.ac.nz/
- Repository: https://ourarchive.otago.ac.nz/
- LinkedIn: https://www.linkedin.com/school/university-of-otago/
- Authentication (Tuakiri SSO): https://ask.otago.ac.nz/knowledgebase/article/KA-10002700/en-us
- Plans: plans/university-of-otago-plans-pricing.yml
- Rate Limits: rate-limits/university-of-otago-rate-limits.yml
- FinOps: finops/university-of-otago-finops.yml
- Review: review.yml

## Notes

- No dedicated public developer portal or documented public API program was found.
- The OUR Archive OAI-PMH endpoint follows the standard Esploro pattern (`/view/oai/64OTAGO_INST/request`); it resolved but returned OAI error_code 21 (unauthorized / harvesting not currently enabled). Confirm authorization with the University of Otago Library before relying on it.
- The legacy DSpace `/oai` path returned 404 after migration to Esploro.
- The main website (https://www.otago.ac.nz/) returns 403 to scripted requests due to bot filtering but is a valid live site.
- A GitHub org named "UniversityofOtago" exists but has no public repositories and is not verifiably official, so it is not catalogued here. Several research-lab orgs (e.g., Gardner-BinfLab, HAM-lab-Otago-University) exist independently and are out of scope for the institutional profile.
- No endpoints were fabricated; all URLs were probed directly. See review.yml for HTTP statuses.

## Maintainers

- Kin Lane — kin@apievangelist.com
