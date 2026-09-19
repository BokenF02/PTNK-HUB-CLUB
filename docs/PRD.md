# PTNK-HUB-CLUB — PRODUCT REQUIREMENTS

DOCUMENT_STATUS: FINAL_LOCK
PRODUCT_SCOPE: ENTIRE_PRODUCT
PURPOSE: DEFINE_PRODUCT_SCOPE_AND_REQUIRED_PRODUCT_CAPABILITIES

---

## 1. PRODUCT_DEFINITION

PTNK-HUB-CLUB is a digital community platform dedicated exclusively to PTNK.

HUB is designed to become the **digital home of PTNK**: a shared environment where students, teachers, alumni, and PTNK clubs can communicate, discover activities, build relationships, share everyday experiences, and preserve community history across generations.

HUB is:

* A PTNK-centered social ecosystem
* A communication and information environment
* A club discovery and community platform
* A long-term memory layer for the PTNK community

HUB is not:

* A generic social network
* A conventional school information website
* A copy of another social platform

External products may provide inspiration, but the resulting experience must be adapted into a distinct PTNK identity.

---

## 2. PRODUCT_PROBLEMS

HUB addresses the following problems:

1. PTNK lacks one shared digital environment connecting its community.
2. School, club, and community information is fragmented across different channels.
3. Students may find conventional information delivery less engaging for everyday communication.
4. Club discovery and participation can be difficult.
5. Student experiences and community history can become fragmented or lost over time.
6. Connections between current students, alumni, teachers, clubs, and generations are difficult to maintain continuously.

---

## 3. PRODUCT_GOALS

HUB aims to:

* Connect the PTNK community in one shared environment.
* Make everyday PTNK communication and information more engaging.
* Help students discover and participate in clubs and activities.
* Enable healthy social interaction and community relationships.
* Preserve meaningful student experiences across generations.
* Maintain connection between students and alumni after graduation.
* Provide a distinct PTNK-specific product identity.
* Establish a foundation that can evolve over many years.

---

## 4. TARGET_USERS_AND_ACTORS

### STUDENT

Students are the primary active community users.

Core needs:

* Consume and create content
* Communicate with others
* Build friendships
* Discover clubs and activities
* Participate in the PTNK community

### TEACHER

Teachers participate in the same social environment as students.

Core needs:

* Consume and create content
* Participate in community activities
* Communicate with the PTNK community

Being a teacher does not automatically imply special community privileges.

### ALUMNI

Former students retain their HUB identity after graduation.

Core needs:

* Remain connected to PTNK
* Follow current school and club activity
* Interact with current and former members
* Continue participating in the community

### CLUB

Clubs are first-class community entities within HUB.

A club can:

* Maintain a community presence
* Publish content
* Share activities
* Promote events
* Manage its community presence and members

Detailed club permissions belong to `PRODUCT_RULES.md`.

### ADMIN

ADMIN is a platform-management role rather than a normal community user category.

Administrative capabilities are defined by product rules and system requirements.

---

## 5. CORE_PRODUCT_EXPERIENCE

HUB is organized around four core experiences:

### COMMUNITY

Connect, communicate, interact, and build relationships within PTNK.

### INFORMATION

Discover school, club, event, and community information through an engaging social environment.

### CLUBS

Discover, follow, explore, and participate in PTNK clubs and their activities.

### MEMORIES

Preserve meaningful student experiences and community history across generations.

These four experiences form the product's core identity.

---

## 6. CORE_PRODUCT_CAPABILITIES

### ACCOUNT_AND_IDENTITY

HUB must support:

* Account creation and authentication
* PTNK-related identity information
* Persistent user identity
* Student → alumni lifecycle
* Profile management

Supported community identities:

* `STUDENT`
* `TEACHER`
* `OSTUDENT`

Administrative access is represented separately by:

* `ADMIN`

Authentication and verification details are implementation/specification concerns.

### PROFILE

Profiles provide a personal representation of a member.

Core capabilities include:

* Identity information
* Avatar
* Bio/basic information
* Social connections
* User content
* Follow/message actions

Profiles may organize different content types into dedicated areas.

### FOLLOW_AND_FRIENDS

HUB uses a follow-based relationship model.

If:

`A follows B` + `B follows A`

then:

`A and B = FRIENDS`

No separate friend-request system is required by the product model.

Friends support social interaction and privacy-related experiences.

### CONTENT

HUB supports community content including:

* Posts
* Images
* Videos
* Albums
* Stories
* Notes
* Mentions
* Other extensible content types

Content must support appropriate interaction and visibility controls.

### FEED

The feed is the primary active community content environment.

It should surface relevant content based on signals such as:

* Relationships
* Clubs
* Interests
* Freshness
* Engagement
* Important school/club content
* Events

The product does not require users to manually choose between separate "Latest" and "Algorithmic" modes.

Feed ranking and recommendation logic are implementation/specification concerns.

### CONTENT_INTERACTION

Supported interaction capabilities include:

* Reactions
* Comments
* Replies
* Sharing
* Saving
* Mentions

Published posts are not edited after publication.

A user who needs to change a post must delete the existing post and create a new one.

Deleted content enters a private Trash area and may be restored according to product rules.

### PRIVACY

Users must have meaningful control over content visibility.

The product supports visibility concepts including:

* `PTNK_COMMUNITY`
* `FRIENDS/FOLLOWERS` where applicable
* `ONLY_ME`

Privacy must remain consistent across the student → alumni transition.

Exact visibility behavior belongs to `PRODUCT_RULES.md`.

### CLUBS

Each club has its own organizational community presence.

Core capabilities include:

* Club profile
* Club content
* Followers
* Activities
* Events
* Media
* Club information/history
* Member management
* Club communication

Club discovery should support search, categories, filters, and future discovery mechanisms.

### MESSAGING

HUB supports:

* Direct 1-to-1 messaging
* Club group communication

User-created arbitrary group chats are not required for V1 unless explicitly approved later.

### EVENTS

Events are a distinct product capability for:

* School events
* Club events
* Official programs
* Appropriate community activities

Events integrate with notifications and relevant discovery surfaces.

### NOTIFICATIONS

Notifications cover major system activity categories:

* Social interactions
* Messages
* School/club events
* System information
* Security-related notifications

Notifications should lead users to the relevant destination rather than duplicating entire content objects.

### SEARCH

HUB provides global search.

V1 search must support at minimum:

* Users
* Posts
* Events

Filters and additional result types may be expanded later.

### VIDEO

Video is a dedicated content experience within HUB.

It may contain content from:

* Students
* Teachers
* Alumni
* Clubs
* Events
* Activities

The video experience must retain HUB's identity rather than directly reproducing another platform's model.

### EMAIL

HUB is intended to provide integrated email capabilities.

Target capabilities include:

* Receive
* Read
* Manage
* Send

Email remains an appropriate channel when communication specifically requires email.

Technical email provider/protocol decisions belong to technical documentation.

### SETTINGS

Settings must provide appropriate controls for:

* Profile/account
* Security
* Content management
* Saved content
* Trash
* Privacy
* Other supported account preferences

Security capabilities may include password management, 2FA, recovery, and session management.

Exact security implementation belongs to `SECURITY.md` and technical documentation.

---

## 7. PTNK_MEMORIES

PTNK Memories is the long-term memory layer of the PTNK student community.

When a student becomes an alumni:

* Their existing student content is preserved in PTNK Memories.
* Existing privacy settings remain respected.
* Their account, identity, relationships, and historical contribution continue.

Alumni may continue creating new content.

New alumni content initially participates in the active community experience and is later preserved in Memories according to the defined product retention rule.

Teacher content does not enter the student-to-alumni Memories lifecycle.

The exact archival period is defined in `PRODUCT_RULES.md`.

---

## 8. SAFETY_AND_MODERATION

HUB must provide mechanisms for:

* Reporting
* Content moderation
* Blocking
* Administrative content actions
* Community safety

The product requires privacy for reporters and appropriate handling of reported content.

Admins may remove content when necessary but must not directly edit user-created content.

Exact:

* report categories
* sanctions
* moderation workflow
* permission boundaries
* enforcement rules

belong to `PRODUCT_RULES.md`.

The exact moderation architecture is not fixed by this PRD.

---

## 9. EXPERIENCE_REQUIREMENTS

### RESPONSIVE

HUB must support:

* Desktop
* Laptop
* Tablet
* Mobile

### LANGUAGES

Initial language requirements:

* Vietnamese
* English

### THEMES

The product supports:

* Light
* Dark
* Theme customization within the HUB design system

### VISUAL_DIRECTION

HUB should feel:

* Young
* Modern
* Smooth
* Distinctive
* High-quality
* Friendly
* Deep rather than superficial
* Community-oriented

The experience must avoid a generic or obviously AI-generated appearance.

### DESIGN_PRINCIPLE

Visual design and animation must serve the experience.

High-impact areas may use stronger interaction and animation.

Task-oriented areas should prioritize speed and clarity.

HUB must develop its own visual and interaction identity rather than directly copying another platform.

Detailed design language belongs to `DESIGN.md`.

---

## 10. QUALITY_REQUIREMENTS

HUB should balance:

`HIGH_QUALITY_EXPERIENCE + STRONG_PERFORMANCE`

The product must not sacrifice usability and performance unnecessarily for visual effects.

The production system should be designed for reliable long-term operation.

Security, scalability, infrastructure, and implementation requirements are defined in technical documentation rather than this PRD.

---

## 11. PRODUCT_VERSIONING

### MVP

MVP is an internal validation release.

Its purpose is to validate:

* Core flows
* System interaction
* UX
* Major technical/product assumptions
* Fundamental platform stability

MVP is not the final product.

### V1

V1 represents the first full usable product foundation.

V1 must implement the core capabilities defined across the approved product documentation, including the major systems for:

* Accounts and profiles
* Social relationships
* Content
* Clubs
* Events
* Messaging
* Notifications
* Video
* PTNK Memories
* Email
* Search
* Settings
* Privacy
* Moderation
* Responsive experience
* Vietnamese and English
* Reusable UI foundations

V1 is a functional product foundation, not a visual prototype.

The exact V1 feature boundary is maintained through `FEATURE-MAP.md` and `ROADMAP.md`.

---

## 12. PRODUCT_EVOLUTION

After V1, HUB evolves through:

* Real user feedback
* Observed product problems
* Community needs
* New validated ideas

A feature must not be added solely because it is trendy or visually interesting.

New features should be evaluated against:

* User value
* PTNK relevance
* Practicality
* UX impact
* System impact
* Long-term maintainability
* Product identity

---

## 13. SUCCESS_CRITERIA

HUB success is not defined primarily by raw user count or vanity metrics.

The core product outcome is:

> Users genuinely value HUB and want to return and participate in the PTNK community.

A successful HUB should make users feel:

* This is our community.
* This is a place where I can connect.
* This is a place where I can share.
* This is a place where I can preserve memories.
* This is a place I can return to even years after graduation.

Real user feedback is an important source for evaluating product quality and future direction.

---

## 14. PRODUCT_BOUNDARY

This PRD defines:

* Product identity and scope
* Problems
* Goals
* Target users and actors
* Core experiences
* Core product capabilities
* Major experience requirements
* Quality expectations
* Product version expectations
* Product evolution principles

This PRD does **not** define:

* Framework selection
* Programming languages
* Database schema
* API architecture
* Folder structure
* Infrastructure
* Deployment architecture
* Exact security implementation
* Exact moderation implementation
* Detailed permission rules
* Detailed retention rules
* Detailed UI specifications

Those concerns belong to their respective documents.

---

## 15. DOCUMENT_RELATIONSHIPS

The product documentation follows a layered flow from product definition toward implementation:

```text
VISION
  ↓
PRD
  ↓
PRODUCT_RULES
  ↓
FEATURE_MAP
  ↓
ROADMAP
  ↓
TECH_ARCHITECTURE
  ↓
SETUP / SECURITY / TUTORIAL
  ↓
CODE
```

Supporting documentation operates alongside this flow:

```text
DESIGN
GROUP_RULES
AGENTS
```

This flow describes documentation responsibility and dependency.

It does not allow a lower-level technical document to silently override an established product decision.

A change that affects an established product decision must update the appropriate source document before being implemented in code.

---

## 16. PRODUCT_PRINCIPLES

PTNK-HUB-CLUB must preserve:

1. `COMMUNITY_FIRST`
2. `PTNK_CENTRIC`
3. `DIGITAL_HOME_OF_PTNK`
4. `MEMORIES_MATTER`
5. `DISTINCT_IDENTITY`
6. `HEALTHY_INTERACTION`
7. `REAL_USER_EXPERIENCE`
8. `LONG_TERM_THINKING`
9. `PRACTICAL_DECISIONS`
10. `BEAUTIFUL_BY_PURPOSE`
11. `RESPECT_THE_COMMUNITY`
12. `ADAPT_NOT_COPY`

---

## 17. FINAL_PRODUCT_STATEMENT

PTNK-HUB-CLUB is the **digital home of PTNK**: a young, modern, distinctive community environment where PTNK members can connect, discover, communicate, share experiences, participate in clubs and activities, and preserve the community's history across generations.

HUB should feel like a **real PTNK community**, not a generic website or an automatically generated social platform.

The product must balance:

`IDENTITY + COMMUNITY + USABILITY + SAFETY + PERFORMANCE + LONG_TERM_CONTINUITY`

---

## FINAL_LOCK

This document defines the confirmed product requirements of PTNK-HUB-CLUB.

Future changes to these requirements must be intentional and documented.

Implementation must follow this document and the other approved project documents.

Unconfirmed technical or implementation decisions must not be inferred from this PRD.
