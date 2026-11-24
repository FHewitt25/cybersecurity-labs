# Lab 7: OWASP Top 10 Investigation

**Focus:** Web application security

## What I did
Researched the OWASP Top 10 (2021) and the OWASP community pages on vulnerabilities and attacks, then documented each item and how to prevent it.

## OWASP Top 10 categories
| Category | What it is | Prevention |
|---|---|---|
| Broken access control | Users can view or edit data they shouldn't, e.g. changing an ID in a URL to reach another account (insecure direct object reference) | Deny by default; enforce authorization checks on the server for every request |
| Injection | Untrusted input is sent to an interpreter (SQL, OS commands) and executed | Parameterized queries, server-side input validation |
| Security misconfiguration | Systems or cloud services set up insecurely (defaults, open ports, verbose errors) | Hardened baselines and automated configuration checks in every environment |

## Attacks
| Attack | What it is | Prevention |
|---|---|---|
| Forced browsing | Guessing URLs to reach unlinked but accessible pages | Don't rely on hidden links; require authentication and authorization on every resource |
| Content spoofing | Injecting content into a trusted page to mislead users | Strictly validate and encode user-supplied input |
| Cryptanalysis | Exploiting weaknesses in crypto to recover plaintext | Use strong, current algorithms and truly random IVs/keys |

## Vulnerabilities
| Vulnerability | What it is | Prevention |
|---|---|---|
| Memory leak | Allocated memory never freed, leading to crashes or denial of service | Careful memory management, code review, testing |
| Covert storage channel | Data leaked through unused or reserved message fields | Zero out reserved fields; send only necessary data |
| Process control | Running commands from an untrusted source or environment | Validate inputs; never execute untrusted commands; run with least privilege |

## Security takeaways
- Broken access control is OWASP's #1 risk, and it's an authorization problem, the same lesson as least privilege in Lab 3.
- Input validation prevents a large share of web attacks.
- As an analyst, knowing these patterns helps me recognize them in web server and WAF logs.
