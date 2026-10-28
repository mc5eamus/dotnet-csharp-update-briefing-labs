# .NET 10 / C# 14 and .NET 11 / C# 15 workshop materials

Customer-facing slide decks and hands-on labs for the two-day .NET and C#
update workshop.

## Slides

The `slides/` directory contains the customer-facing HTML decks:

- [Day 1 — .NET 10 / C# 14](slides/day1.html)
- [Day 2 — .NET 11 / C# 15](slides/day2.html)
- [Source registry](slides/sources.html)

Clone or download the repository and open the files locally. Each page is
self-contained, works without a network connection, and excludes speaker
notes.

## Day 1 code examples

The Day 1 examples are available as complete starter and solution projects:

- [Lab 01 — C# 14](Day1/01-CSharp14)
- [Lab 02 — PQC and JSON hardening](Day1/02-Libraries-Pqc-Json)
- [Lab 03 — Minimal API and OpenAPI](Day1/03-AspNetCore-OpenApi)
- [Lab 04 — EF Core 10](Day1/04-EfCore10)

## Day 2 code examples

The Day 2 examples are available as complete starter and solution projects:

- [Lab 05 — Runtime Async](Day2/05-RuntimeAsync)
- [Lab 06 — C# 15 unions and closed hierarchies](Day2/06-CSharp15-Unions)
- [Lab 07 — .NET 11 libraries](Day2/07-Libraries11)
- [Lab 08 — ASP.NET Core 11 migration](Day2/08-AspNet11-Migration)
- [Lab 09 — EF Core 11 migration](Day2/09-EfCore11-Migration)

The repository contains nine labs. Every lab has:

- a `README.md` exercise brief;
- a `start/` project for attendees;
- a `solution/` project for comparison and facilitator verification.

## Prerequisites

- .NET 10 SDK for the Day 1 labs
- .NET 11 SDK RC 1 or later for the Day 2 labs
- Visual Studio, VS Code with C# Dev Kit, Rider, or another C# editor

Install both SDKs side by side. The .NET 11 SDK can build existing `net10.0`
projects, but its templates do not scaffold a `net10.0` project.

Post-quantum cryptography in Lab 02 also depends on operating-system support.
The lab checks `IsSupported` and remains usable when an algorithm is unavailable.

## Get started

```powershell
git clone https://github.com/mc5eamus/dotnet-csharp-update-briefing-labs.git
cd dotnet-csharp-update-briefing-labs

dotnet build Day1.sln
dotnet build Day2.sln
```

The attendee solutions contain only the `start/` projects. Facilitators can
also build the completed implementations:

```powershell
dotnet build Day1-Solutions.sln
dotnet build Day2-Solutions.sln
```

## Labs

| Day 1 — .NET 10 / C# 14 | Day 2 — .NET 11 / C# 15 |
|---|---|
| `01-CSharp14` | `05-RuntimeAsync` |
| `02-Libraries-Pqc-Json` | `06-CSharp15-Unions` |
| `03-AspNetCore-OpenApi` | `07-Libraries11` |
| `04-EfCore10` | `08-AspNet11-Migration` — upgrades Lab 03 |
| | `09-EfCore11-Migration` — upgrades Lab 04 |

Day 2 currently targets the .NET 11 RC 1 packages used to verify the workshop.
Re-check those pinned packages when .NET 11 reaches GA.

## License

Licensed under the [MIT License](LICENSE).
