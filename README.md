# mdma — Mail Domain Mail Analysis

A command-line tool that queries and displays DNS and mail-related records for a given domain.

## Usage

```sh
mdma <domain.tld>
```

## Output

For the supplied domain, `mdma` prints:

- **A/AAAA records** — host addresses
- **PTR records** — reverse DNS of each A/AAAA address
- **MX records** — mail exchangers, sorted by priority
- **mail.\<domain\>** — A record for the `mail.` subdomain
- **SPF record** — the full SPF record, with all nested `include:` chains resolved recursively
- **NS records** — authoritative name servers

## Dependencies

`host(1)`, `dig(1)`, `awk(1)`, `grep(1)`, `cut(1)`