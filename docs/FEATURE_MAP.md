# PTNK-HUB-CLUB — FEATURE MAP

```yaml
DOCUMENT_STATUS: FINAL_LOCK
DOCUMENT_SCOPE: PRODUCT_FEATURE_MAP
PURPOSE: DEFINE_MAJOR_PRODUCT_FEATURES_AND_THEIR_RELATIONSHIPS
```

---

## 1. DOCUMENT PURPOSE

This document defines the major functional areas of PTNK-HUB-CLUB and their relationships.

Feature Map answers:

> What major capabilities exist in HUB, and how are they organized?

This document does not define implementation details.

It does not define:

* Programming languages
* Frameworks
* Databases
* APIs
* Infrastructure
* Deployment
* Detailed UI specifications
* Detailed security implementation
* Detailed moderation workflows
* Detailed permission matrices
* Development schedules

Confirmed behavioral and operational rules are defined in `PRODUCT-RULES.md`.

---

# 2. FEATURE STATUS

Features in this document use the following status concepts:

### CONFIRMED

The feature is part of the currently defined product scope.

### TBD

The feature exists or is expected, but specific behavior or details have not yet been decided.

### FUTURE_IDEA

The feature is an intended future direction but is not part of the currently locked scope.

### OUT_OF_SCOPE

The feature has been explicitly excluded from the current product scope.

Undecided features must not be treated as confirmed requirements.

---

# 3. ACCOUNT & IDENTITY

Account and Identity establishes a user's identity and role within HUB.

## Roles

Supported platform roles include:

* `STUDENT`
* `TEACHER`
* `OSTUDENT`
* `ADMIN`
* Club-scoped roles

## Registration & Identity

Registration is based on PTNK-issued Gmail accounts.

The system should identify the appropriate role for the person rather than treating every registrant as the same account type.

The registration experience may collect information such as:

* Full name
* Class
* Club participation

Club participation is optional.

A user may belong to no club.

The exact identity-verification and role-assignment process is not defined in this Feature Map.

## Student → OSTUDENT

When a student becomes an `OSTUDENT`:

* The account remains
* Existing data remains
* Existing relationships remain
* Existing interactions remain
* Existing content remains
* Eligible historical content enters PTNK Memories
* Original content privacy remains preserved

---

# 4. PERSONAL PROFILE

Personal Profile represents a user's identity and personal presence within HUB.

A profile may include:

* Avatar
* Name
* Nickname
* Identity information
* Biography
* Followers
* Following
* Total likes
* Social links
* Follow
* Message

## Profile Content

Profile content areas include:

* Posts
* Photos
* Videos
* Albums
* Stories
* Notes

## Friends

Friends are derived from the Follow relationship.

```text
Follow
   +
Mutual Follow
   ↓
Friends
```

There is no separate Friend Request system.

Users can view and discover their Friends through supported profile and relationship features.

---

# 5. HOME

Home is the primary entry point into the PTNK community.

Home may provide access to:

* PTNK identity
* HUB identity
* Club discovery
* Community content
* Highlighted / notable content
* Main navigation
* Footer

Home should have its own PTNK-HUB-CLUB identity.

It should not simply reproduce another social platform's structure or visual identity.

---

# 6. CLUBS

Clubs are active community spaces within HUB.

## Club Profile

A club profile may include:

* Logo
* Name
* Introduction
* Followers
* Follow
* Posts
* Photos
* Videos
* Albums
* Activities
* Events
* Club information
* Club history

Club achievements and activities are represented through club profile and content rather than through a separate achievement system.

## Club Management

Authorized club leaders and deputy leaders may manage permitted club areas, including:

* Club profile
* Club content
* Events
* Members
* Media
* Club group chat
* Activities

Club management is subject to the rules and limits defined in `PRODUCT-RULES.md`.

## Club Discovery

Club discovery may include:

* Categories
* Filters
* Keywords
* Search
* Additional discovery mechanisms introduced later

---

# 7. FEED & CONTENT

Feed is a primary community content experience.

## Content Types

HUB supports content such as:

* Posts
* Images
* Videos
* Albums
* Stories
* Notes
* Feelings
* Mentions

Video is a supported content type within posts. It is not currently defined as a separate video platform.

Location-based content is outside the current scope.

## Feed Algorithm

The Feed uses algorithmic ranking.

Ranking may consider signals such as:

* Time
* Likes / reactions
* Comments
* Views
* Engagement
* Follow / Friend relationships
* Interests
* Community interest / relevance

The existence of algorithmic ranking is confirmed.

The exact ranking formula, weights, implementation, and future optimization are not defined in this document.

Users do not currently choose between a separate chronological Feed mode and an algorithmic Feed mode.

---

# 8. CONTENT INTERACTION

Content may support:

* Like / Reaction
* Comment
* Reply
* Share
* Save
* Mention

Content owners may have controls such as:

* Removing comments on their content
* Disabling comments where supported

Detailed permissions are governed by `PRODUCT-RULES.md`.

---

# 9. PRIVACY & VISIBILITY

Supported visibility levels include:

* `PTNK COMMUNITY`
* `FRIENDS`
* `ONLY ME`

Visibility applies according to the supported content type.

When eligible content enters PTNK Memories, its original privacy and visibility must remain preserved.

---

# 10. CONTENT MANAGEMENT

## Published Content

Published posts cannot be edited.

If a user wants to change a published post:

```text
Delete existing post
        ↓
Create new post
```

## Trash

Deleted content may enter Trash.

Authorized users may:

* View deleted content
* Restore eligible content

Trash access is restricted to the content owner or authorized user.

## Saved

Users have a personal Saved area.

Supported actions include:

* View
* Manage
* Remove from Saved

---

# 11. PTNK MEMORIES

PTNK Memories preserves meaningful PTNK community experiences across generations.

When:

```text
STUDENT
   ↓
OSTUDENT
```

eligible historical student content enters the Memories lifecycle.

The original privacy and visibility of the content remain preserved.

Alumni content may also enter the Memories lifecycle according to the rules defined in `PRODUCT-RULES.md`.

Teacher content does not follow the student-to-alumni Memories lifecycle.

---

# 12. FOLLOW & FRIENDS

Follow relationships may exist between appropriate HUB identities, including:

* Students
* Teachers
* Alumni
* Clubs

Relationship model:

```text
Follow
   +
Mutual Follow
   ↓
Friends
```

There is no separate Friend Request system.

---

# 13. MESSAGING

## Direct Messaging

Users can communicate through 1-to-1 messaging.

## Club Group Chat

Clubs have dedicated group communication.

Club group chat is part of the current feature scope.

User-created arbitrary group chats are outside the current scope.

---

# 14. EVENTS

Events are a supported product capability.

Current confirmed Event scope includes:

* Club Events
* Other Event experiences defined by the product as development progresses

Events may connect with Notifications.

Personal activities do not require a separate personal Event system and may instead be represented through supported content such as Posts.

## School Events

A dedicated School Events direction is currently treated as:

```yaml
STATUS: FUTURE_IDEA
```

It may be developed later as HUB evolves.

---

# 15. NOTIFICATIONS

Notifications provide relevant community and system updates.

## Social

Examples include:

* Follow
* Like / Reaction
* Comment
* Reply
* Relevant interactions

## Messaging

Examples include:

* New messages
* Relevant messaging activity

## Club / Event

Club or event-related updates may appear as notification items that lead to the relevant content or Event detail.

## System

Examples include:

* Maintenance
* Feature updates
* Rule changes
* Security alerts

---

# 16. PTNK EMAIL

PTNK Email integration is a future development direction.

```yaml
STATUS: FUTURE_IDEA
```

The intended direction may include:

* Receive
* Read
* Manage
* Send

The integration method, provider, authentication, access, synchronization, and implementation are not currently locked.

---

# 17. SEARCH

HUB provides system-wide search.

Current primary search areas include:

* Users
* Posts
* Events

Additional searchable areas may be added later.

---

# 18. SAFETY

## Report

Users can report supported content or accounts.

The system may support multiple report categories.

## Block

Users can block other users.

Blocking may affect relevant areas such as:

* Messaging
* Follow relationships
* Content interaction
* Visibility

Detailed blocking behavior and moderation procedures are defined outside this Feature Map.

---

# 19. ADMIN

Admin provides authorized operational management of the platform.

Major areas include:

* Users
* Permissions
* Reports
* Violations
* Authorized content actions
* Operational data

Admin may take action against violating content or users when sufficient grounds exist and according to the applicable rules.

This may include:

* Removing violating content
* Restricting users
* Suspending or banning users for defined periods

Exact violation categories, evidence requirements, durations, procedures, and permissions are governed by `PRODUCT-RULES.md` and later detailed rules.

Admin does not independently determine product direction.

Admin does not directly edit user-created content.

Admin does not own or manage the official source code / codebase as a product ownership function.

---

# 20. SETTINGS

## Profile

Supported profile settings may include:

* Profile customization
* Background gradient / image
* Account information
* Other system-supported personalization

## Security

Security capabilities include:

* Password management
* Two-Factor Authentication (2FA)
* Account recovery
* Session management
* Logout from individual devices
* Logout from all devices

### Two-Factor Authentication

2FA is a built-in security capability.

Users can:

* Enable 2FA
* Disable 2FA

The exact authentication method is:

```yaml
STATUS: TBD
```

## Content

Content-related settings may include:

* Saved
* Trash
* Other personal content controls

The current scope does not include an automatic account-deletion workflow based on a waiting period followed by permanent deletion.

---

# 21. UI & PLATFORM EXPERIENCE

## Responsive

HUB is intended to support:

* Desktop
* Laptop
* Tablet
* Mobile

## Languages

* Vietnamese
* English

## Theme

HUB supports:

* Light Mode
* Dark Mode
* Supported interface customization

Detailed visual language and aesthetic direction are defined in `DESIGN.md`.

---

# 22. CURRENT OUT-OF-SCOPE ITEMS

The following are explicitly outside the current scope:

* Location-based content
* Separate Friend Request system
* User-created arbitrary group chats
* Separate achievement system for clubs
* Automatic account deletion through a waiting-period workflow
* Separate video platform independent from post content

This list is intentionally limited to decisions that have been explicitly established.

The absence of an item from this list does not automatically mean the item is required or prohibited.

---

# 23. FUTURE IDEAS

The following directions are recognized but are not currently locked as core implementation scope:

* PTNK Email integration
* Dedicated School Events experience
* Additional club discovery mechanisms
* Additional search areas
* Other community capabilities identified through future product development

Future ideas must not be treated as current confirmed requirements until explicitly promoted into the confirmed product scope.

---

# 24. FEATURE RELATIONSHIP

```text
ACCOUNT & IDENTITY
├── Personal Profile
│   ├── Posts
│   ├── Photos
│   ├── Videos
│   ├── Albums
│   ├── Stories
│   └── Notes
├── Follow / Friends
├── Messaging
│   └── Club Group Chat
├── Notifications
├── Saved
├── Trash
└── Settings
    ├── Profile
    ├── Security
    │   ├── 2FA
    │   ├── Account Recovery
    │   └── Session Management
    └── Content

HOME
├── Club Discovery
│   └── Club Profile
│       ├── Content
│       ├── Media
│       ├── Activities
│       ├── Events
│       └── Management
└── Community Content

COMMUNITY
├── Feed
│   └── Algorithmic Ranking
├── Content
│   ├── Posts
│   ├── Images
│   ├── Videos
│   ├── Albums
│   ├── Stories
│   ├── Notes
│   └── Feelings
├── Events
├── PTNK Memories
├── Search
└── Notifications

SAFETY
├── Report
└── Block

ADMIN
├── Users
├── Permissions
├── Reports
├── Violations
├── Content Actions
└── Operational Management

FUTURE IDEAS
├── PTNK Email
└── School Events
```

---

# 25. FEATURE EVOLUTION

Feature Map may be expanded as HUB develops.

New features should:

* Have a clear product purpose
* Remain consistent with `VISION.md`
* Remain consistent with `PRD.md`
* Respect confirmed rules in `PRODUCT-RULES.md`
* Have a clear status before being treated as confirmed
* Avoid introducing technical implementation details into this document

Uncertain details should remain explicitly marked as `TBD` rather than being silently converted into confirmed requirements.

Future ideas should remain separate from current confirmed scope until intentionally promoted.

---

# 26. DOCUMENT RELATIONSHIP

Feature Map sits between Product Rules and Roadmap:

```text
VISION
   ↓
PRD
   ↓
PRODUCT-RULES
   ↓
FEATURE-MAP
   ↓
ROADMAP
   ↓
TECH-ARCHITECTURE
   ↓
IMPLEMENTATION
```

The responsibilities are:

* `VISION.md` → Long-term identity and direction
* `PRD.md` → Product requirements and goals
* `PRODUCT-RULES.md` → Confirmed operational and behavioral rules
* `FEATURE-MAP.md` → Major product capabilities and their relationships
* `ROADMAP.md` → Development sequence and timing
* `TECH-ARCHITECTURE.md` → Technical architecture and implementation structure

Feature Map must not replace or silently override these documents.

---

# 27. FINAL STATUS

```yaml
DOCUMENT_STATUS: FINAL_LOCK
LOCK_SCOPE: FEATURE_MAP
CHANGES_REQUIRE: EXPLICIT_REVIEW
```
