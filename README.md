# UNSC Fleetnet

Public geofeed for UNSC Fleetnet.

## Geofeed

Consumer URL: https://ksmoove21.github.io/unsc-fleetnet/geofeed.csv

[Source CSV](geofeed.csv). Use the HTTPS consumer URL above rather than GitHub's HTML blob page.

The October 28, 2026 [publication commit](https://github.com/ksmoove21/unsc-fleetnet/commit/75f1687164207bb24d0478f8b140f8d81b120e1d) identifies Waldorf, Maryland, United States as the intended geolocation for both entries. This is an operator-published geographic assertion, not independent verification of physical equipment location.

## Resource and publication audit

Checked October 29, 2026. Registry assignment, contractual usage rights, routing authorization, and geographic intent are distinct evidence.

| Prefix | Current authoritative registry evidence | Evidence boundary |
| --- | --- | --- |
| `2a06:9801:15d0::/44` | RIPE exact-prefix record: `UNSC-NET-44`, status `ASSIGNED`, organization `ORG-KP140-RIPE` (Kendall Powell), administrative/technical contact `KP5583-RIPE`, maintained by `LAGRANGE-AUTO-MNT`. Created 2026-10-26 16:16:42 UTC; last modified 2026-10-27 03:24:14 UTC. | Confirms registered assignment to the operator's organization under Lagrange's parent allocation. Does not establish a transfer of the parent allocation or independent property ownership. |
| `104.128.232.0/24` | ARIN exact-prefix record: `NET-104-128-232-0-1`, name `OVH-2`, active `ASSIGNMENT`, registrant CloudWish LLC (`CL-2297`). Parent `104.128.224.0/20`: `HOSTUS-IPV4-2`. | Operator confirms a HostUS lease. A supplied HostUS Solutions LLC LOA dated October 28, 2026 explicitly authorizes Kendall Powell to announce this /24 via AS218293 and related peers, customers and upstreams. Announcement authorization is now document-supported; lease terms and title are not established by the LOA. ARIN lists CloudWish LLC as the exact-prefix registrant; the HostUS/CloudWish registration relationship remains unreconciled. |

The /44 covers `2a06:9801:15d0::` through `2a06:9801:15df:ffff:ffff:ffff:ffff:ffff` (16 /48s). It does not contain the previously documented `2a06:9801:15c1::/48`; no replacement or surrender is inferred.

### Supplied authorization evidence

Reviewed October 29, 2026. Provider documents supplied by the operator support announcement authorization as follows; issuer authenticity and revocation status were not independently checked. The private documents are not published here.

| Prefix | Issuer | LOA date | Authorized origin |
| --- | --- | --- | --- |
| `104.128.232.0/24` | HostUS Solutions LLC | October 28, 2026 | AS218293 |
| `2602:fed2:719c::/48` | Free Range Cloud Ltd. | October 24, 2026 | AS218293 |
| `2a06:9801:15c1::/48` | Lagrange Cloud | October 23, 2026 | AS218293 |
| `2a06:9801:15d0::/44` | Lagrange Cloud | October 26, 2026 | AS218293 |

The IPv6 letters state that authorization continues until revoked or modified in writing. These documents establish documentary authorization, not proof of current BGP propagation, legal ownership, or geofeed registration.

### Format and delivery

- Both rows pass UTF-8 CSV parsing, five-field validation and strict canonical CIDR checks.
- `US` and `US-MD` identify the United States and Maryland. City is `Waldorf`; the optional postal-code field is blank.
- No CSV header is required. No overlapping or duplicate entries are present.
- The consumer URL returned HTTP 200 with `text/csv; charset=utf-8`, and its contents matched the repository CSV.
- CSV formatting follows [RFC 8805](https://www.rfc-editor.org/rfc/rfc8805.html). Registry discovery follows [RFC 9632](https://www.rfc-editor.org/rfc/rfc9632.html).

### Registry discovery gap

No geofeed URL was present in the exact-prefix RIPE inet6num record or ARIN RDAP network record during this audit. The inspected RIPE /29 parent and ARIN /20 parent also contained no geofeed reference. A working public URL alone does not establish registry-based discovery or geolocation-provider ingestion. This audit does not claim an exhaustive search of every possible less-specific record or third-party feed index.

The relevant authorized maintainer should publish the consumer URL in the RIPE /44's `geofeed:` attribute. For IPv4, announcement authorization is supported by the HostUS LOA; confirm with HostUS which authorized maintainer can arrange the registry geofeed reference. The LOA does not itself register or authorize editing a registry object. These registry changes have not been performed or verified.

No prefix or geographic data was changed: no substantiated CSV error was found. No BGP advertisements, ROAs, IRR route objects, or operational configurations were modified.

### Authoritative sources

- [RIPE /44 RDAP](https://rdap.db.ripe.net/ip/2a06:9801:15d0::)
- [RIPE /44 inet6num](https://rest.db.ripe.net/ripe/inet6num/2a06:9801:15d0::%2F44.json)
- [RIPE parent allocation](https://rest.db.ripe.net/ripe/inet6num/2a06:9800::%2F29.json)
- [ARIN /24 RDAP](https://rdap.arin.net/registry/ip/104.128.232.0)
- [ARIN parent allocation](https://rdap.arin.net/registry/ip/104.128.224.0/20)
