# PTNK HUB CLUB — ROADMAP

> Roadmap phát triển PTNK HUB CLUB từ nền tảng sản phẩm đến vận hành thực tế và phát triển lâu dài.
>
> **Deadline xây dựng chính:** giữa tháng 10/2027  
> **Mục tiêu:** sản phẩm chạy thực tế, ổn định, có thể duy trì và tiếp tục phát triển qua các roadmap tiếp theo.

---

## 1. ROADMAP PRINCIPLES

- Xây dựng dựa trên các quyết định đã được xác nhận; không tự ý thay đổi.
- Không tự thêm framework, database, infrastructure, tool, function hoặc architecture khi chưa được nghiên cứu và quyết định.
- Phân biệt rõ `LOCKED`, `OPEN DECISION`, `PROPOSAL`, `CONFLICT`.
- Nếu có conflict ảnh hưởng đến implementation, phải xác định và giải quyết trước khi tiếp tục phần bị ảnh hưởng.
- Team gồm 3 người và cùng đi qua các Period.
- Không bắt buộc chia team thành các chuyên môn cố định.
- Người nhận task chịu trách nhiệm chính với task đó.
- Task thông thường nên được giới hạn khoảng 1 tuần.
- Cuối mỗi tuần phải test và review.
- Cả 3 thành viên cùng tham gia test/review.
- Học công nghệ trong quá trình làm project; không cần một giai đoạn học riêng.
- UX/UI được cải thiện liên tục trong quá trình phát triển.
- Task khó có thể cần nhiều thời gian hơn để giữ đúng yêu cầu.
- Không hy sinh chất lượng chỉ để giữ deadline trên giấy.
- Sau khi website ổn định, feedback thực tế được dùng để quyết định các cải tiến.
- Deadline chính không phải điểm kết thúc tuyệt đối; sau đó có thể tạo roadmap mới.

---

# 2. ROADMAP OVERVIEW

```text
PERIOD 0 — PRODUCT FOUNDATION
        ↓
PERIOD 1 — SPECIFICATION
        ↓
PERIOD 2 — PLANNING
        ↓
PERIOD 3 — TASKS
        ↓
PERIOD 4 — DEVELOPMENT
        ↓
PERIOD 5 — TESTING / HARDENING
        ↓
PERIOD 6 — DEPLOYMENT
        ↓
PERIOD 7 — FEEDBACK / OPTIMIZATION
        ↓
NEW ROADMAP — LONG-TERM EVOLUTION
```

Mỗi Period có:
- Objective
- Main work
- Completion gate

---

# 3. PERIOD 0 — PRODUCT FOUNDATION

## Objective

Hoàn thiện và chốt nền tảng sản phẩm, workflow của team, workflow AI, định hướng technical architecture và yêu cầu security trước khi đi vào SPEC.

## Sequence

```text
PRD
 ↓
ROADMAP
 ↓
SETUP
TUTORIAL
GROUP_RULES
AGENTS
 ↓
TECH-ARCHITECTURE
 ↓
SECURITY
 ↓
REVIEW + LOCK PERIOD 0
 ↓
SPEC
```

## Existing documents

- `VISION.md` — đã hoàn thành.
- `PRODUCT_RULES.md` — đã hoàn thành.
- `FEATURE_MAP.md` — đã hoàn thành.
- `PRD.md` — các yêu cầu chính đã được thu thập; cần tối ưu và chốt.

## Documents to complete

- `ROADMAP.md`
- `SETUP.md`
- `TUTORIAL.md`
- `GROUP_RULES.md`
- `AGENTS.md`
- `TECH-ARCHITECTURE.md`
- `SECURITY.md`

## Main work

1. Finalize `PRD.md`.
2. Create and lock `ROADMAP.md`.
3. Document environment/setup in `SETUP.md`.
4. Document project structure and beginner workflow in `TUTORIAL.md`.
5. Define team workflow in `GROUP_RULES.md`.
6. Define AI/Agent behavior in `AGENTS.md`.
7. Define technical architecture in `TECH-ARCHITECTURE.md` without inventing unresolved technology decisions.
8. Define security requirements in `SECURITY.md`.
9. Cross-check the foundation documents.
10. Resolve important conflicts.
11. Review and lock Period 0.

## Completion gate

Period 0 is complete only when:

- Required foundation documents exist.
- Important decisions are locked or explicitly marked `OPEN DECISION`.
- Important conflicts are resolved.
- Team understands the workflow.
- Architecture is sufficiently defined for SPEC.
- Security requirements are sufficiently defined for SPEC.
- Team has reviewed and locked Period 0.

---

# 4. PERIOD 1 — SPECIFICATION

## Objective

Chuyển product requirements thành specifications đủ chi tiết để có thể implementation.

## Main work

For each relevant module:

1. Read locked source documents.
2. Define scope.
3. Define behavior.
4. Define states and transitions.
5. Define permissions.
6. Define relevant data requirements.
7. Define errors and edge cases.
8. Define important UX/UI behavior.
9. Define acceptance criteria.
10. Cross-check against source documents.

Possible specification areas:

```text
Account
Profile
Follow / Friends
Home
Feed / Content
Clubs
Messaging
Events
Notifications
Video
PTNK Memories
Email
Search
Reports / Safety
Settings
Admin
...
```

Danh sách trên là định hướng phân module từ Feature Map, không phải tự động thêm feature mới.

## Important rule

**SPEC là documentation, không phải CODE.**

AI/Skills có thể hỗ trợ tạo SPEC nhưng team phải review và lock.

## Completion gate

- Required modules have specifications.
- Specifications are consistent with locked product requirements.
- Important states, edge cases and acceptance criteria are documented.
- Open decisions are explicitly marked.
- No important specification gap blocks PLAN.

---

# 5. PERIOD 2 — PLANNING

## Objective

Chuyển SPEC thành một implementation plan thực tế.

## Main work

- Xác định thứ tự implementation.
- Xác định dependencies.
- Xác định technical prerequisites.
- Nhóm work thành các milestone phù hợp.
- Ước lượng theo năng lực thực tế của team.
- Xác định testing/review points.
- Đối chiếu với deadline giữa tháng 10/2027.
- Điều chỉnh khi tiến độ thực tế khác kế hoạch.

## Planning rules

- Không bắt buộc hệ thống version cố định.
- Không chia team thành chuyên môn cố định.
- Giữ đầy đủ requirements khi có thể.
- Task khó được phép cần thêm thời gian.
- Nếu delay ảnh hưởng roadmap, phải cập nhật kế hoạch.

## Completion gate

- Implementation order rõ.
- Dependencies rõ.
- Milestones có time window hợp lý.
- Có thể chuyển thành TASKS.
- Kế hoạch phù hợp deadline chính.

---

# 6. PERIOD 3 — TASKS

## Objective

Chia PLAN thành các task rõ ràng để từng thành viên có thể nhận và thực hiện.

## Structure

```text
MODULE / EPIC
    ↓
FEATURE
    ↓
TASK
    ↓
SUBTASK (nếu cần)
```

## Each task should contain

- Objective.
- Scope.
- Related documents/specifications.
- Dependencies.
- Owner.
- Completion criteria.
- Testing expectations.

## Default task cycle

```text
TASK
 ↓
CODE + LEARN
 ↓
~1 WEEK
 ↓
TEAM TEST
 ↓
TEAM REVIEW
 ↓
PASS → MERGE / NEXT TASK
FAIL → FIX → TEST + REVIEW AGAIN
```

Task có thể kéo dài hơn nếu thực sự cần thiết, nhưng ảnh hưởng phải được thể hiện trong roadmap/plan.

## Completion gate

- Tasks đủ nhỏ để thực hiện.
- Không cần đoán requirements.
- Dependencies rõ.
- Có thể assign và track.

---

# 7. PERIOD 4 — DEVELOPMENT

## Objective

Xây dựng product thực tế theo SPEC, PLAN và TASKS.

## Development flow

```text
TASK
 ↓
READ RELEVANT DOCS
 ↓
UNDERSTAND
 ↓
CODE + LEARN
 ↓
SELF-CHECK
 ↓
ALL 3 TEST
 ↓
ALL 3 REVIEW
 ↓
PASS → MERGE
FAIL → FIX → TEST + REVIEW
```

## Team model

- 3 thành viên cùng tham gia.
- Không yêu cầu permanent Frontend/Backend/UI split.
- Task owner chịu trách nhiệm chính.
- Các thành viên hỗ trợ nhau.
- Học trong lúc xây dựng.

## AI / Freebuff

AI là development assistant, không phải authority của product.

Khi dùng Freebuff:

- Cung cấp task rõ ràng.
- Cho AI đọc các docs liên quan.
- Giữ implementation trong scope của task.
- Không để AI tự thay đổi locked product decisions.
- Không để AI tự quyết định architecture chưa được chốt.
- Review code do AI tạo.
- Test code do AI tạo.
- Không mặc định AI-generated code là đúng.

## UX/UI direction

UX/UI được tối ưu liên tục.

HUB cần duy trì:

- Modern, young, smooth experience.
- PTNK/HUB identity rõ.
- High-quality purposeful effects.
- Animation có kiểm soát theo từng khu vực.
- Cân bằng WOW và performance.
- Trải nghiệm không mang cảm giác website được AI tạo đại trà.
- Không sao chép trực tiếp design/content/experience của nền tảng khác.

## Completion gate

Task/module chỉ được coi là hoàn thành khi:

- Implementation đáp ứng task.
- Test đạt.
- Team review đạt.
- Important bugs được xử lý.
- Documentation liên quan được cập nhật nếu cần.

---

# 8. PERIOD 5 — TESTING / HARDENING

## Objective

Kiểm tra toàn hệ thống trước khi đưa vào vận hành thực tế.

## Testing scope

Tùy feature và toàn hệ thống:

- Functional testing.
- Integration testing.
- Responsive testing.
- UI/UX testing.
- Performance testing.
- Security testing.
- Browser compatibility.
- Accessibility.
- Error handling.
- Edge cases.
- Community safety.

## Two testing levels

### Continuous testing

Mỗi task:

```text
TASK
 ↓
TEAM TEST
 ↓
TEAM REVIEW
```

### Full-system testing

Trước deployment:

```text
FULL SYSTEM
 ↓
INTEGRATED TEST
 ↓
HARDENING
 ↓
FINAL REVIEW
```

## Critical bug flow

```text
CRITICAL BUG
 ↓
ISOLATE / STOP AFFECTED PART IF NECESSARY
 ↓
FIX
 ↓
RETEST
 ↓
TEAM REVIEW
 ↓
RETURN TO SYSTEM
```

Không che giấu critical bug để giữ deadline.

## Completion gate

- Required functionality works.
- Responsive behavior acceptable.
- UX/UI acceptable.
- Critical issues handled.
- Security reviewed.
- Performance reviewed.
- System ready for deployment.

---

# 9. PERIOD 6 — DEPLOYMENT

## Objective

Đưa product từ development/test environment vào vận hành thực tế.

## Main work

- Prepare production environment.
- Prepare production configuration.
- Verify deployment workflow.
- Verify security.
- Verify data handling.
- Prepare backup/recovery where required.
- Prepare monitoring/logging where required.
- Prepare rollback/recovery.
- Perform final production checks.

## Deployment principle

**Chạy được trên máy developer không có nghĩa là production-ready.**

Test environment và production environment phải được kiểm tra riêng.

## Primary target

Đạt trạng thái sản phẩm chạy thực tế khoảng **giữa tháng 10/2027**.

---

# 10. PERIOD 7 — FEEDBACK / OPTIMIZATION

## Objective

Sau khi product ổn định, dùng trải nghiệm thực tế và feedback để xác định các cải tiến tiếp theo.

## Initial feedback approach

Hiện tại feedback có thể được thu thập thủ công/trực tiếp.

Feedback system chính thức sẽ được quyết định sau.

## Improvement cycle

```text
REAL FEEDBACK
 ↓
DISCUSS / ANALYZE
 ↓
EVALUATE NEED
 ↓
SELECT CHANGE
 ↓
CREATE TASK
 ↓
IMPLEMENT
 ↓
TEST + REVIEW
 ↓
RELEASE
```

## Rules

- Feedback không tự động trở thành requirement.
- Feature mới phải được đánh giá thực tế.
- Không thêm feature chỉ vì đang trend.
- Thay đổi quan trọng phải nhất quán với product foundation.
- Thay đổi locked rules phải được xác nhận trước implementation.

---

# 11. LONG-TERM EVOLUTION — NEW ROADMAP

Roadmap này **không phải điểm kết thúc của HUB**.

Sau khi product vận hành:

```text
CURRENT ROADMAP
      ↓
REAL-WORLD OPERATION
      ↓
FEEDBACK + NEW IDEAS
      ↓
EVALUATION
      ↓
NEW ROADMAP
      ↓
FURTHER DEVELOPMENT
      ↓
NEW ROADMAP...
```

Các hướng tương lai dưới đây chỉ là khả năng, **không phải commitment**:

- UX improvements.
- Performance improvements.
- Feature improvements.
- Community safety improvements.
- Operational improvements.
- Maintenance.
- Developer succession/transfer.
- Potential transfer to school.
- Future platform expansion.

Mỗi hướng phải được đánh giá khi thực sự cần.

---

# 12. WEEKLY DEVELOPMENT CYCLE

```text
START OF WEEK
        ↓
TASK ASSIGNED
        ↓
READ SPEC + RELATED DOCS
        ↓
CODE + LEARN
        ↓
SELF-CHECK
        ↓
END OF WEEK
        ↓
ALL 3 TEST
        ↓
ALL 3 REVIEW
        ↓
┌─────────────────┐
│ PASS            │
│ → MERGE         │
│ → NEXT TASK     │
└─────────────────┘

OR

┌─────────────────┐
│ FAIL            │
│ → FIX           │
│ → TEST AGAIN    │
│ → REVIEW AGAIN  │
└─────────────────┘
```

### Timing

- Default task: khoảng 1 tuần.
- Task khó: có thể kéo dài.
- Delay phải được nhìn thấy.
- Roadmap/plan được cập nhật khi thực tế thay đổi.
- Không đánh dấu unfinished work là complete chỉ để giữ deadline.

---

# 13. PERIOD COMPLETION GATE

Một Period chỉ được `DONE` khi các điều kiện áp dụng đã đạt:

```text
REQUIRED WORK COMPLETE
        +
TEST COMPLETE
        +
REVIEW COMPLETE
        +
DOCUMENTATION UPDATED
        +
IMPORTANT CONFLICTS RESOLVED
        =
PERIOD DONE
```

Việc viết xong document hoặc code xong **không tự động có nghĩa Period đã hoàn thành**.

---

# 14. DECISION STATES

## `LOCKED`

Quyết định đã được xác nhận.

→ Các công việc phía sau phải tôn trọng quyết định này cho đến khi được thay đổi chính thức.

## `OPEN DECISION`

Chưa quyết định.

→ Không được tự đoán thành requirement.

## `PROPOSAL`

Đề xuất để xem xét.

→ Chưa phải requirement chính thức.

## `CONFLICT`

Có từ hai nguồn/decision trở lên không thống nhất.

→ Phải xác định và giải quyết trước khi phần bị ảnh hưởng tiếp tục.

---

# 15. SOURCE OF TRUTH

```text
VISION.md
PRODUCT_RULES.md
FEATURE_MAP.md
PRD.md
        ↓
TECH-ARCHITECTURE.md
SECURITY.md
        ↓
SPEC
        ↓
PLAN
        ↓
TASKS
        ↓
CODE
```

## Change propagation

Nếu một quyết định nền tảng cần thay đổi:

```text
IDENTIFY NEED
 ↓
DISCUSS / EVALUATE
 ↓
CONFIRM CHANGE
 ↓
UPDATE SOURCE DOCUMENT
 ↓
UPDATE DEPENDENT DOCUMENTS
 ↓
REVIEW IMPACT
 ↓
CONTINUE
```

Document cấp thấp không được tự ý override document cấp cao đã locked.

---

# 16. DEADLINE MANAGEMENT

## Primary deadline

**Giữa tháng 10/2027**

Đây là constraint chính của roadmap.

## Strategy

- Mỗi Period có time window hợp lý.
- Task thông thường khoảng 1 tuần.
- Weekly testing/review bắt buộc.
- Task khó được phép cần thêm thời gian.
- Nếu delay ảnh hưởng các Period sau, phải tính lại.
- Không đánh dấu unfinished work là complete chỉ để giữ deadline.

**Exact dates của từng Period sẽ được chốt sau khi Period 0 hoàn thiện và năng lực thực tế của team được kiểm tra.**

---

# 17. FINAL TARGET

Khoảng **giữa tháng 10/2027**, PTNK HUB CLUB hướng tới trạng thái:

- Product chạy thực tế.
- Các chức năng đã được định nghĩa được implementation.
- Core experiences đã được test.
- Responsive đã được test.
- UX/UI được tối ưu liên tục.
- Security đã được review.
- Performance đã được review.
- Critical issues được xử lý.
- Deployment workflow đã được thiết lập.
- Có foundation để maintain và phát triển lâu dài.

**Đây không phải end-of-project tuyệt đối.**

Đây là endpoint của roadmap hiện tại và là điểm bắt đầu cho các roadmap tiếp theo.

---

# 18. CURRENT ROADMAP STATUS

| Item | Status |
|---|---|
| Primary deadline | **Mid-October 2027** |
| Team | **3 members** |
| Task ownership | **Individual owner per task** |
| Normal task duration | **~1 week** |
| Weekly testing | **Required** |
| Weekly review | **Required** |
| Testers | **All 3 members** |
| Learning model | **Learn while building** |
| UX/UI | **Continuous improvement** |
| Main delivery target | **Real-world operation** |
| Post-deadline | **Create a new roadmap and continue** |

---

# 19. NEXT ACTION

Sau khi `ROADMAP.md` được chấp nhận:

```text
ROADMAP.md
 ↓
SETUP.md
 ↓
TUTORIAL.md
 ↓
GROUP_RULES.md
 ↓
AGENTS.md
 ↓
TECH-ARCHITECTURE.md
 ↓
SECURITY.md
 ↓
REVIEW + LOCK PERIOD 0
 ↓
SPEC
```

Không được coi Period 0 là hoàn thành cho đến khi **Period 0 Completion Gate** được đáp ứng.
