# Hackathon Brief: Codegeist 2026: Build with context. Ship with confidence.

- Devpost URL: https://codegeist2026.devpost.com/
- Prize Pool: $<span data-currency-value>120,000</span>
- Deadline: about 2 months left
- Approval Status: ✅ APPROVED BY USER
- Approved Product Name: MedTrace GxP Compliance Guardian (Apps for Specialized Industries)
- Approved Pitch: Hệ thống tự động kiểm toán truy xuất nguồn gốc (Traceability Matrix) chuẩn FDA 21 CFR Part 11 & ISO 13485 dành cho đội ngũ phần mềm y tế/dược phẩm: liên kết yêu cầu thiết kế trên Confluence, đánh giá rủi ro FMEA và bằng chứng kiểm thử trên Jira qua Forge + Rovo Agent để xuất hồ sơ thẩm định kiểm toán chỉ trong 1 click.
- Winning Angle: Đánh vào hạng mục ít cạnh tranh nhất là Apps for Specialized Industries ($15k), giải quyết nỗi đau kiểm toán pháp lý cực đắt đỏ trong ngành y tế/sinh học thay vì các công cụ dev thông thường.
- Required Stack: Atlassian Forge (Storage, Triggers & Custom UI), Atlassian Rovo Agent & Reusable Skills (rovo:agent, rovo:skill), Teamwork Graph API, Jira & Confluence Cloud API, TypeScript / React
- Studio Harness Root: `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`

## Studio Harness Engineering Rules (SDD → VSDD → CoDD)

1. **Product & Architecture (`studio.design.init` + `studio.product.specification`)**:
   - Đọc `.claude/commands/design-init.md` và `.claude/commands/spec.md`.
   - Tạo `DESIGN.md` và `SPEC.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/SPEC.md`) bám sát ý tưởng đã được duyệt (`MedTrace GxP Compliance Guardian (Apps for Specialized Industries)`), với các tiêu chí nghiệm thu định dạng `- AC-1: <hành vi kiểm chứng được>`, `- AC-2: ...`.
   - Chạy `npm --prefix /Volumes/AllySSD/Projects/AgentAppStudio/studio-harness run coverage:check -- --spec ./SPEC.md` đảm bảo trả về danh sách tiêu chí hợp lệ (exit code 0).
2. **Engineering (`studio.build.implement`)**:
   - Đọc `.claude/commands/build.md`, xây dựng ứng dụng hoàn chỉnh chạy thực tế ở cổng 3000 (hoặc 8000), không dùng mock data cứng.
   - Viết test kiểm chứng cho từng tiêu chí `AC-*` và đảm bảo build + test pass 100%.
3. **Review, QA & Release (`studio.validate.gate` + `studio.validate.cto-review`)**:
   - Đọc `.claude/commands/validate.md` và `.claude/commands/cto.md`.
   - Tạo `VALIDATION.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/VALIDATION.md`) ánh xạ từng `AC-*` tới bằng chứng test/build thực tế.
   - Tạo `SUBMISSION.md` theo đúng chuẩn Devpost (gồm các mục: `## Elevator Pitch`, `## Inspiration`, `## What it does`, `## How we built it`, `## Challenges we ran into`, `## Accomplishments that we're proud of`, `## What's next`) và vẽ sơ đồ Mermaid.js trong `README.md`.
