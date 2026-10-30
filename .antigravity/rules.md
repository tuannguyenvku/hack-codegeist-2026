# Hackathon Brief: Codegeist 2026: Build with context. Ship with confidence.

- Devpost URL: https://codegeist2026.devpost.com/
- Prize Pool: $<span data-currency-value>120,000</span>
- Deadline: about 2 months left
- Approval Status: ✅ APPROVED BY USER
- Approved Product Name: ContextPulse AI
- Approved Pitch: Mỗi kỹ sư sở hữu một Agent ngầm tự động đối chiếu mã nguồn (Bitbucket PR) với yêu cầu thiết kế (Confluence) và tiến độ sprint (Jira) trong thời gian thực, phát hiện sớm sai lệch ngữ cảnh (context drift) trước khi merge. Nền tảng tự động sinh bài kiểm thử chấp nhận (acceptance verification) và cấp thẻ chứng nhận 'Ship with Confidence Scorecard' cho từng pull request.
- Winning Angle: Đánh trúng 100% chủ đề 'Build with context. Ship with confidence' của Atlassian bằng kiến trúc Forge native kết hợp Atlassian Rovo Agents, biến luồng tra cứu thụ động thành trợ lý bối cảnh chủ động theo chuẩn One-Agent-Per-User.
- Required Stack: Atlassian Forge (Custom UI & Triggers), Atlassian Rovo Agent SDK, TypeScript / React, OpenAI / Claude API, Bitbucket & Jira REST API
- Studio Harness Root: `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`

## Studio Harness Engineering Rules (SDD → VSDD → CoDD)

1. **Product & Architecture (`studio.design.init` + `studio.product.specification`)**:
   - Đọc `.claude/commands/design-init.md` và `.claude/commands/spec.md`.
   - Tạo `DESIGN.md` và `SPEC.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/SPEC.md`) bám sát ý tưởng đã được duyệt (`ContextPulse AI`), với các tiêu chí nghiệm thu định dạng `- AC-1: <hành vi kiểm chứng được>`, `- AC-2: ...`.
   - Chạy `npm --prefix /Volumes/AllySSD/Projects/AgentAppStudio/studio-harness run coverage:check -- --spec ./SPEC.md` đảm bảo trả về danh sách tiêu chí hợp lệ (exit code 0).
2. **Engineering (`studio.build.implement`)**:
   - Đọc `.claude/commands/build.md`, xây dựng ứng dụng hoàn chỉnh chạy thực tế ở cổng 3000 (hoặc 8000), không dùng mock data cứng.
   - Viết test kiểm chứng cho từng tiêu chí `AC-*` và đảm bảo build + test pass 100%.
3. **Review, QA & Release (`studio.validate.gate` + `studio.validate.cto-review`)**:
   - Đọc `.claude/commands/validate.md` và `.claude/commands/cto.md`.
   - Tạo `VALIDATION.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/VALIDATION.md`) ánh xạ từng `AC-*` tới bằng chứng test/build thực tế.
   - Tạo `SUBMISSION.md` theo đúng chuẩn Devpost (gồm các mục: `## Elevator Pitch`, `## Inspiration`, `## What it does`, `## How we built it`, `## Challenges we ran into`, `## Accomplishments that we're proud of`, `## What's next`) và vẽ sơ đồ Mermaid.js trong `README.md`.
