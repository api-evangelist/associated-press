# Associated Press GraphQL Schema

## Overview

This GraphQL schema represents the conceptual data model for the Associated Press (AP) content and media APIs. The AP provides developer APIs for accessing news content, photos, video, audio, graphics, and election data produced by AP's global newsgathering operations. This schema covers the core entities available through the AP Media API, AP Content API, and related services documented at https://developer.ap.org/ap-media-api/.

## Schema Source

Derived from the AP Media API and AP Content API developer documentation at https://developer.ap.org/. The REST API surfaces entities for stories, media objects, bureaus, journalists, feeds, and account management that are modeled here as a GraphQL type system.

## Types

### Content Types

- **Story** — A news article or wire story produced by AP correspondents. Central content entity containing metadata, body text, headline, and associated media.
- **StoryDetails** — Extended metadata for a story including editorial classifications, transmission info, and versioning data.
- **StoryContent** — The body content of a story, including structured paragraphs, embedded media references, and formatting.
- **Headline** — The primary headline for a story, with support for multiple headline variants.
- **Subheadline** — A secondary or supplementary headline providing additional context below the main headline.
- **Summary** — A short abstract or summary of a story for previews and aggregation feeds.
- **Byline** — The byline field attributing authorship of a story to one or more journalists or the AP wire.
- **BylineCredits** — Detailed credit information for all contributors to a story's byline.
- **Dateline** — The dateline indicating the location from which a story was filed.
- **StoryCategory** — Editorial category classification for a story (e.g., Sports, Politics, Business).
- **Subject** — A structured IPTC subject designation applied to a story for topical classification.
- **SubjectCode** — The numeric or alphanumeric IPTC subject code identifying a subject classification.
- **StoryKeyword** — A free-text keyword tag applied to a story for search and discovery.
- **IPTCCategory** — An IPTC media topic category code used in AP's editorial taxonomy.
- **Language** — The language in which a story or media asset is written or produced.
- **Urgency** — The editorial urgency level assigned to a story (e.g., Routine, Urgent, Bulletin, Flash).
- **Priority** — The transmission priority for a story on the AP wire.
- **EditorialType** — The editorial type classification of a story (e.g., Analysis, Feature, Breaking News).
- **StoryVersion** — A specific version of a story in the AP content system, tracking editorial revisions.
- **StoryRevision** — A tracked revision to a story, capturing changes between versions.
- **TransmissionInfo** — Metadata about the wire transmission of a story, including sequence numbers and transmission dates.
- **TransmissionDate** — The date and time a story was transmitted on the AP wire.

### Media Types

- **MediaObject** — The base type for all media assets in the AP content system, including photos, videos, audio, and graphics.
- **Photo** — A news photograph produced by AP photographers or licensed to AP.
- **PhotoDetails** — Extended metadata for a photo including technical specifications and editorial context.
- **PhotoCaption** — The caption text associated with a news photograph.
- **PhotoCredit** — Credit attribution for a photograph including photographer name and agency.
- **Photographer** — A photographer who contributed an image to the AP photo archive.
- **PhotoDate** — The date a photograph was taken or transmitted.
- **PhotoCategory** — The editorial category of a photograph (e.g., News, Sports, Entertainment).
- **PhotoSize** — A specific rendition or size variant of a photograph available for download.
- **Video** — A news video clip or package produced by AP video journalists.
- **VideoDetails** — Extended metadata for a video asset including duration, format, and editorial notes.
- **VideoCaption** — The caption or script associated with a video asset.
- **VideoCredit** — Credit attribution for a video including journalist and production details.
- **VideoThumbnail** — A still image thumbnail extracted from or associated with a video asset.
- **VideoDuration** — The runtime duration of a video asset.
- **VideoFormat** — The encoding format and resolution specifications for a video rendition.
- **Audio** — An audio clip or package produced by AP radio or broadcast services.
- **AudioDetails** — Extended metadata for an audio asset including duration, format, and editorial context.
- **AudioCaption** — Caption or script text associated with an audio asset.
- **Graphic** — An infographic, chart, or interactive graphic produced by AP graphics team.
- **GraphicDetails** — Extended metadata for a graphic asset including format and dimensions.
- **MediaPackage** — A bundled collection of related media assets associated with a story or event.

### Organization Types

- **Bureau** — An AP news bureau or office location contributing content to the wire.
- **BureauDetails** — Extended details about a bureau including address, region, and coverage area.
- **Region** — A geographic region designation used to categorize AP bureau and content coverage.
- **Country** — A country entity associated with story datelines, bureau locations, or subject geography.
- **City** — A city associated with a story dateline or bureau location.

### Personnel Types

- **Journalist** — An AP staff journalist, photographer, or video journalist contributing content.
- **JournalistProfile** — Profile information for a journalist including bio and contact details.
- **JournalistBeat** — The editorial beat or coverage area assigned to a journalist.

### Distribution Types

- **SourceFeed** — An AP content feed or wire service subscription delivering content to customers.
- **CustomerAccount** — An account for an AP API customer or subscriber organization.
- **ContentAccess** — Access control and entitlement information defining what content a customer can retrieve.
- **Rights** — Rights and licensing metadata associated with a media asset or story.

### Authentication and API Types

- **APIKey** — An API key credential used to authenticate requests to AP developer APIs.
- **Token** — An authentication token used for session-based API access.
- **Webhook** — A webhook endpoint configured to receive push notifications for AP content events.

## Queries

- `story(id: ID!)` — Retrieve a single story by its AP content identifier.
- `stories(feedId: ID, category: String, urgency: Urgency, language: String, limit: Int, offset: Int)` — List stories with optional filtering by feed, category, urgency, and language.
- `photo(id: ID!)` — Retrieve a single photo by its AP media identifier.
- `photos(category: String, photographer: String, dateFrom: String, dateTo: String, limit: Int, offset: Int)` — Search photos with filters.
- `video(id: ID!)` — Retrieve a single video asset by identifier.
- `videos(category: String, dateFrom: String, dateTo: String, limit: Int, offset: Int)` — Search video assets.
- `mediaPackage(id: ID!)` — Retrieve a media package by identifier.
- `bureau(id: ID!)` — Retrieve bureau details by identifier.
- `bureaus(region: String, country: String)` — List bureaus filtered by region or country.
- `journalist(id: ID!)` — Retrieve journalist profile by identifier.
- `sourceFeed(id: ID!)` — Retrieve a source feed definition by identifier.
- `sourceFeeds(accountId: ID!)` — List feeds available to a customer account.
- `customerAccount(id: ID!)` — Retrieve customer account information.

## Mutations

- `createWebhook(input: WebhookInput!)` — Register a webhook endpoint for AP content event notifications.
- `updateWebhook(id: ID!, input: WebhookInput!)` — Update an existing webhook configuration.
- `deleteWebhook(id: ID!)` — Remove a webhook registration.

## References

- AP Developer Portal: https://developer.ap.org/
- AP Media API Documentation: https://developer.ap.org/ap-media-api/
- AP Elections API Documentation: https://developer.ap.org/ap-elections-api/
