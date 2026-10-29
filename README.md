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
| `104.128.232.0/24` | ARIN exact-prefix record: `NET-104-128-232-0-1`, name `OVH-2`, active `ASSIGNMENT`, registrant CloudWish LLC (`CL-2297`). Parent `104.128.224.0/20`: `HOSTUS-IPV4-2`. | Public registry evidence does not establish UNSC's lease, subdelegation, or ownership. It also does not disprove a private lease. Provider delegation or contractual evidence remains necessary. |

The /44 covers `2a06:9801:15d0::` through `2a06:9801:15df:ffff:ffff:ffff:ffff:ffff` (16 /48s). It does not contain the previously documented `2a06:9801:15c1::/48`; no replacement or surrender is inferred.

### Format and delivery

- Both rows pass UTF-8 CSV parsing, five-field validation and strict canonical CIDR checks.
- `US` and `US-MD` identify the United States and Maryland. City is `Waldorf`; the optional postal-code field is blank.
- No CSV header is required. No overlapping or duplicate entries are present.
- The consumer URL returned HTTP 200 with `text/csv; charset=utf-8`, and its contents matched the repository CSV.
- CSV formatting follows [RFC 8805](https://www.rfc-editor.org/rfc/rfc8805.html). Registry discovery follows [RFC 9632](https://www.rfc-editor.org/rfc/rfc9632.html).

### Registry discovery gap

No geofeed URL was present in the exact-prefix RIPE inet6num record or ARIN RDAP network record during this audit. The inspected RIPE /29 parent and ARIN /20 parent also contained no geofeed reference. A working public URL alone does not establish registry-based discovery or geolocation-provider ingestion. This audit does not claim an exhaustive search of every possible less-specific record or third-party feed index.

The relevant authorized maintainer should publish the consumer URL in the RIPE /44's `geofeed:` attribute. For IPv4, first establish the operator's delegation with the provider, then arrange an appropriate registry geofeed reference through the authorized holder using the registry's supported mechanism. These registry changes have not been performed or verified.

No prefix or geographic data was changed: no substantiated CSV error was found. No BGP advertisements, ROAs, IRR route objects, or operational configurations were modified.

### Authoritative sources

- [RIPE /44 RDAP](https://rdap.db.ripe.net/ip/2a06:9801:15d0::)
- [RIPE /44 inet6num](https://rest.db.ripe.net/ripe/inet6num/2a06:9801:15d0::%2F44.json)
- [RIPE parent allocation](https://rest.db.ripe.net/ripe/inet6num/2a06:9800::%2F29.json)
- [ARIN /24 RDAP](https://rdap.arin.net/registry/ip/104.128.232.0)
- [ARIN parent allocation](https://rdap.arin.net/registry/ip/104.128.224.0/20)
