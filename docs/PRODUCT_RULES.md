# PTNK-HUB-CLUB — PRODUCT RULES

DOCUMENT_STATUS: FINAL_LOCK
PRODUCT_SCOPE: ENTIRE_PRODUCT
PURPOSE: DEFINE_CONFIRMED_PRODUCT_RULES_AND_OPERATIONAL_CONSTRAINTS

---

## 1. DOCUMENT_PURPOSE

`PRODUCT_RULES.md` defines the confirmed product rules, permissions, constraints, and operational principles of PTNK-HUB-CLUB.

This document does not define:

* Development workflow
* Team collaboration rules
* AI agent behavior
* Technical architecture
* Implementation details

Those concerns belong to their respective documents.

Only confirmed product rules should be locked here.

Unconfirmed rules must remain explicitly `TBD` or be deferred until a decision is made.

---

## 2. OWNERSHIP

Current ownership:

* Product ownership belongs to the Founder.

Future ownership:

* Ownership may be transferred to the school or another appropriate entity.
* Transfer is not automatic.
* A transfer must be based on an intentional decision.

Ownership, administration, development, and data responsibilities may belong to different entities.

A change in ownership does not automatically change the product's established identity, principles, or core requirements.

---

## 3. ROLES

### `STUDENT`

Current PTNK student.

### `TEACHER`

PTNK teacher.

By default, TEACHER has the same basic community-level capabilities as STUDENT.

The `TEACHER` role primarily identifies the user's community identity.

Teacher-specific privileges are not implied unless explicitly defined.

### `OSTUDENT`

Former PTNK student / alumni.

OSTUDENT retains the user's HUB identity after graduation.

### `ADMIN`

Platform administrator responsible for authorized operational and moderation tasks.

### CLUB_ROLES

Club roles apply only within the corresponding club.

Club-specific permissions do not automatically grant platform-wide privileges.

Current product-level club leadership includes:

* Club Leader
* Club Deputy Leader

Detailed permission boundaries are defined in the Club Rules below.

---

## 4. COMMUNITY_ROLE_BASELINE

The following community identities currently share the same basic platform-level permission baseline:

* `STUDENT`
* `TEACHER`
* `OSTUDENT`

Additional role-specific permissions may be introduced only through an explicit product decision.

`ADMIN` is a separate platform-management role.

Club roles are scoped to their respective clubs.

---

## 5. ADMIN_RULES

ADMIN is responsible for authorized platform-management activities, including:

* User management
* Permission management
* Content moderation
* Violation handling
* Report handling
* Authorized administrative data operations
* Other system-supported administrative tasks

ADMIN must not:

* Independently decide the product's direction
* Silently change core product requirements
* Independently redefine the product's identity
* Directly edit user-created content

Where content action is required, ADMIN may remove or otherwise handle content according to the applicable product rules.

Administrative authority must remain subject to the established product rules and appropriate accountability.

ADMIN privileges may be revoked when there is an appropriate basis and process.

---

## 6. DEVELOPER_RULES

The initial development team consists of:

* 3 Developers
* Equal standing
* No Developer Leader

Developers are responsible for:

* Development
* Maintenance
* Bug fixing
* Upgrades
* New product versions
* Technical integrity

The Developers are not employees of a company by default.

HUB is an independent product.

Developer responsibilities must not be interpreted as automatic ownership of the product.

### DEVELOPER_SUCCESSION

If the Developer team needs to be changed:

* The 3 original Developers make the decision.
* Initial Developer succession requires unanimous agreement: `3/3`.

When the Founder graduates, development responsibility may be transferred to other appropriate Developers through an intentional decision.

Detailed team workflow belongs to `GROUP_RULES.md`.

---

## 7. CLUB_RULES

Club roles are valid only within the corresponding club.

Authorized club leaders may manage the club capabilities granted to them, including:

* Club information
* Club content
* Club activities
* Club members
* Other authorized club functions

Club leaders and deputy leaders may directly update their club's information without requiring prior ADMIN approval, subject to system rules, safety mechanisms, and applicable limits.

### SENSITIVE_CLUB_CHANGES

Sensitive changes may be rate-limited.

Confirmed example:

* Club name: maximum `1 change / 3 days`

Other sensitive-change limits are currently:

`TBD`

The system must not invent additional limits without an explicit product decision.

---

## 8. COMMUNITY_CONTENT

Users may create and share content supported by HUB.

Under normal conditions:

* Content does not require ADMIN approval before publication.
* Users must follow community rules.
* Users may report violating content.
* Violating content may be handled according to moderation rules.

The exact moderation workflow is not fixed by this document.

---

## 9. CONTENT_EDITING

Published posts cannot be edited.

If a user needs to change a published post:

1. Delete the existing post.
2. Create a new post with the desired content.

Deleted content enters the user's private Trash area.

Restoration behavior is subject to the applicable product and system rules.

---

## 10. PRIVACY_AND_VISIBILITY

Supported content visibility levels include:

* `PTNK_COMMUNITY`
* `FRIENDS`
* `ONLY_ME`

The system may process the minimum information required to operate the product.

Personal information must not be exposed beyond the user's permitted visibility scope, except where information is necessary for legitimate system operation.

Privacy must remain respected during the Student → OSTUDENT transition.

Detailed visibility behavior for specific content types may be defined separately when required.

---

## 11. FRIENDSHIP_RULE

HUB uses a follow-based relationship model.

If:

```text
A follows B
+
B follows A
=
FRIENDS
```

No separate friend-request system is required.

Friend status may affect:

* Social interaction
* Content visibility
* Messaging
* Other product experiences

Detailed behavior must follow the applicable product rules.

---

## 12. STUDENT_TO_OSTUDENT_RULE

When a STUDENT graduates:

* Their HUB identity is retained.
* Their account remains active.
* Their relationships are retained.
* Their historical contributions are retained.
* Existing student content enters the PTNK Memories lifecycle.
* Their privacy settings remain respected.

The user becomes:

`STUDENT → OSTUDENT`

Graduation does not automatically remove the user's participation in HUB.

---

## 13. PTNK_MEMORIES_RULES

### STUDENT_CONTENT

Student content remains in the normal active social environment while the user is a STUDENT.

When the user becomes an OSTUDENT:

* Existing student content is preserved in PTNK Memories.
* Existing privacy requirements remain respected.

### ALUMNI_CONTENT

OSTUDENT users may continue creating new content.

New OSTUDENT content:

1. Appears in the active community experience.
2. Remains active for a defined period.
3. Is subsequently preserved in PTNK Memories.

The exact archival period is:

`TBD`

### TEACHER_CONTENT

Teacher content does not enter the Student → OSTUDENT Memories lifecycle.

---

## 14. EMAIL_RULES

HUB is intended to integrate with the PTNK email environment.

Target capabilities include:

* Receiving email
* Reading email
* Managing email
* Connecting email experiences with HUB

The following remain:

`TBD`

* Email provider
* Protocol
* Access model
* Data synchronization model
* Authentication method
* Detailed security requirements

No technical integration method is implied by this product rule.

---

## 15. MODERATION_AND_REPORTING

HUB must support the basic product capabilities required for community safety, including:

* Reporting
* Moderation
* Blocking
* Administrative content actions
* Violation handling

Reporters must receive appropriate privacy protection.

ADMIN may take authorized action against violating content.

ADMIN must not directly rewrite user-created content.

The following are not fully defined here and remain subject to future product decisions:

* Report categories
* Sanction levels
* Exact moderation workflow
* Enforcement durations
* Automated moderation architecture
* Detailed permission boundaries

---

## 16. OWNERSHIP_TRANSFER_RULES

If HUB ownership is transferred, the following must be considered separately:

* Product ownership
* Platform administration
* Development responsibility
* Data management
* Data usage authority

Transfer of one responsibility does not automatically transfer all other responsibilities.

Specific transfer conditions and procedures are:

`TBD`

Ownership transfer must not silently invalidate confirmed product principles.

---

## 17. RULE_EXPANSION

New product rules should be added only when there is sufficient basis for making the decision.

Do not prematurely lock rules that are not yet understood.

New rules may be introduced when:

* A real product requirement appears.
* An existing ambiguity needs resolution.
* A safety or privacy requirement requires clarification.
* A new feature creates a necessary product constraint.
* A confirmed decision changes an existing rule.

When a new rule conflicts with an established product decision, the relevant source document must be intentionally updated.

---

## 18. RULE_STATUS

Rules in this document follow these principles:

### `CONFIRMED`

An explicitly decided product rule.

### `TBD`

A product decision that has not yet been finalized.

### `DEFERRED`

A decision intentionally postponed until a later product stage.

AI agents and developers must not treat `TBD` or `DEFERRED` items as confirmed requirements.

---

## FINAL_LOCK

This document contains the confirmed product rules currently established for PTNK-HUB-CLUB.

Future changes must be intentional, documented, and consistent with the higher-level product vision and requirements.

Technical implementation must follow these rules without silently redefining them.

Unconfirmed decisions must not be inferred from this document.
