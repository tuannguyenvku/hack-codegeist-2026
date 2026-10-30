# Hackathon Brief: Codegeist 2026: Build with context. Ship with confidence.

- Devpost URL: https://codegeist2026.devpost.com/
- Prize Pool: $<span data-currency-value>120,000</span>
- Deadline: about 2 months left
- Selected Winning Idea: AI Context Agent for Jira/Confluence tự động đồng bộ tài liệu PRD thành task backlog và sprint tracking thông minh
- Required Stack: Atlassian Forge, TypeScript, Gemini API, React
- Studio Harness Root: `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`

## Studio Harness Engineering Rules (SDD → VSDD → CoDD)

1. **Product & Architecture (`studio.design.init` + `studio.product.specification`)**:
   - Đọc `.claude/commands/design-init.md` và `.claude/commands/spec.md`.
   - Tạo `DESIGN.md` và `SPEC.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/SPEC.md`) với các tiêu chí nghiệm thu định dạng `- AC-1: <hành vi kiểm chứng được>`, `- AC-2: ...`.
   - Chạy `npm --prefix /Volumes/AllySSD/Projects/AgentAppStudio/studio-harness run coverage:check -- --spec ./SPEC.md` đảm bảo trả về danh sách tiêu chí hợp lệ (exit code 0).
2. **Engineering (`studio.build.implement`)**:
   - Đọc `.claude/commands/build.md`, xây dựng ứng dụng hoàn chỉnh chạy thực tế ở cổng 3000 (hoặc 8000), không dùng mock data cứng.
   - Viết test kiểm chứng cho từng tiêu chí `AC-*` và đảm bảo build + test pass 100%.
3. **Review, QA & Release (`studio.validate.gate` + `studio.validate.cto-review`)**:
   - Đọc `.claude/commands/validate.md` và `.claude/commands/cto.md`.
   - Tạo `VALIDATION.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/VALIDATION.md`) ánh xạ từng `AC-*` tới bằng chứng test/build thực tế.
   - Tạo `SUBMISSION.md` theo đúng chuẩn Devpost (gồm các mục: `## Elevator Pitch`, `## Inspiration`, `## What it does`, `## How we built it`, `## Challenges we ran into`, `## Accomplishments that we're proud of`, `## What's next`) và vẽ sơ đồ Mermaid.js trong `README.md`.
