# AGENTS.md — Codegeist 2026: Build with context. Ship with confidence.

Hướng dẫn cho AI agents (Antigravity `agy` & Studio Harness) làm việc trên repo này.

## Project

Sản phẩm dự thi Hackathon **Codegeist 2026: Build with context. Ship with confidence.** (Đã được người dùng phê duyệt ý tưởng):
- **Tên sản phẩm**: ContextPulse AI
- **Mô tả**: ContextPulse AI: Mỗi kỹ sư sở hữu một Agent ngầm tự động đối chiếu mã nguồn (Bitbucket PR) với yêu cầu thiết kế (Confluence) và tiến độ sprint (Jira) trong thời gian thực, phát hiện sớm sai lệch ngữ cảnh (context drift) trước khi merge. Nền tảng tự động sinh bài kiểm thử chấp nhận (acceptance verification) và cấp thẻ chứng nhận 'Ship with Confidence Scorecard' cho từng pull request.
- **Góc độ thắng giải**: Đánh trúng 100% chủ đề 'Build with context. Ship with confidence' của Atlassian bằng kiến trúc Forge native kết hợp Atlassian Rovo Agents, biến luồng tra cứu thụ động thành trợ lý bối cảnh chủ động theo chuẩn One-Agent-Per-User.
- **Quy trình kỹ thuật**: **SDD → VSDD → CoDD** của `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`.

## Architectural decisions (đọc trước khi sửa)

| Quyết định | Lý do | Ngày |
|---|---|---|
| Chốt ý tưởng `ContextPulse AI` | Đã qua bước Human Approval Gate trước khi build | 2026-10 |
| Áp dụng Studio Harness (`SDD → VSDD → CoDD`) | Đảm bảo mọi tính năng đều có `DESIGN.md`, `SPEC.md` (`AC-1..N`), test tự động và `VALIDATION.md` | 2026-10 |

## Known gaps (đừng "sửa nhầm")

- Chưa có (cập nhật trong quá trình chạy `/build` và `/validate`).

## Structure aliases (SPEC ↔ code)

- `SPEC.md` → Đặc tả hệ thống & danh sách `- AC-1: ...`
- `DESIGN.md` → Hệ thống thiết kế UI/UX
- `VALIDATION.md` → Báo cáo nghiệm thu theo chuẩn Studio Harness
- `SUBMISSION.md` → Bài thuyết trình nộp Devpost
