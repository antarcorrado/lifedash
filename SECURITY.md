# Security policy

## Reporting a vulnerability

Please report security problems **privately**, through GitHub's
[«Report a vulnerability»](https://github.com/antarcorrado/lifedash/security/advisories/new)
form (Security tab of this repository). The report stays visible only to you and
the maintainer until a fix is out.

Please do not open a public issue, and do not test against other people's accounts
or data. On the official server (`www.antarcorrado.com/lifedash`) only use accounts
you created yourself, and do not run load tests or automated scans that could
disrupt it.

A useful report says what is affected (Mac app, web app, `lifedash` command or
server, and the version), how to reproduce it, and what an attacker could gain.

You will get an answer within a few days. Once a fix is released the advisory is
published, crediting you if you wish.

## Supported versions

Only the latest release receives security fixes. The Mac app updates itself; the
web app always runs the server's current version.

## Scope

In scope: the Mac app, the web app, the `lifedash` command, the sync server and its
encryption protocol.

Out of scope: problems that need an already compromised device, social engineering,
and reports from automated scanners without a concrete impact.

How LifeDash protects data, and its known limits, are described in
[`server/SECURITY.md`](server/SECURITY.md) (in Italian) once the server code is
public.
