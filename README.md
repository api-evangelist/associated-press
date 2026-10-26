# Associated Press (associated-press)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

The Associated Press (AP) is an American not-for-profit news agency founded in 1846. The AP is the world's oldest and largest newsgathering organization, serving media companies worldwide with text, photos, video, audio, and interactive content. The AP provides developer APIs for accessing election data, news content, and media assets including the AP Elections API for real-time election results, the AP Content API for news and media asset access, and the AP Media API for digital asset management integration.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/associated-press/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Elections, Journalism, Media, News, Content

## Timestamps

- **Created:** 2024-04-14
- **Modified:** 2026-04-19

## APIs

### AP Elections API
Integrate your election systems with AP Elections API. Your election results delivery application retrieves election race information from AP Elections API to power election websites, reporting systems, and news dashboards. Provides real-time election results, candidate data, and race call information for federal, state, and local elections.

**Human URL:** [https://developer.ap.org/ap-elections-api/](https://developer.ap.org/ap-elections-api/)

#### Tags:

 - Elections, News, Results

#### Properties

- [Documentation](https://developer.ap.org/ap-elections-api/)
- [GettingStarted](https://developer.ap.org/ap-elections-api/)

### AP Media API
The AP Media API provides access to AP's digital media assets including photos, videos, and graphics from AP's global newsgathering operations. Enables integration with digital asset management systems and content management platforms for news organizations.

**Human URL:** [https://developer.ap.org/](https://developer.ap.org/)

#### Tags:

 - Media, Photos, Video, Content

#### Properties

- [Documentation](https://developer.ap.org/)
- [OpenAPI](openapi/associated-press-meda-openapi-original.yml)

## Common Properties

- [Associated Press Website](https://www.ap.org/)
- [AP Developer Portal](https://developer.ap.org/)
- [Developer Documentation](https://developer.ap.org/)

## Artifacts

### OpenAPI

- [AP Media API](openapi/associated-press-meda-openapi-original.yml)

## Features

| Name | Description |
|------|-------------|
| AP Elections API | Real-time election results delivery for federal, state, and local elections with candidate data, race calls, and vote totals. |
| AP Content API | Access to AP's global news content including text stories, photos, video, and graphics from AP correspondents worldwide. |
| AP Media API | Digital asset management integration for AP's extensive photo and video library with metadata, rights, and distribution capabilities. |
| AP DataStream | Streaming news content delivery for applications requiring real-time news updates and content ingestion. |

## Use Cases

| Name | Description |
|------|-------------|
| Election Coverage | News organizations and election management companies use the AP Elections API to power live election result dashboards and reporting. |
| News Content Integration | Media companies integrate AP content APIs to supplement their own coverage with AP newswire stories and multimedia content. |
| Photo and Video Licensing | Publishers and digital media companies access AP's photo and video archive through the Media API for editorial and commercial use. |

## Integrations

| Name | Description |
|------|-------------|
| Newsroom CMS Integrations | AP content APIs integrate with major content management systems used by newspapers, broadcasters, and digital media publishers. |
| Election Management Systems | Election technology vendors integrate AP Elections API for authoritative election result data in voting systems and election night reporting tools. |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
