# AGENTS.md — Codegeist 2026: Build with context. Ship with confidence.

Hướng dẫn cho OpenAI Codex CLI (`codex`) & Studio Harness làm việc trên repo này.

## Project

Sản phẩm dự thi Hackathon **Codegeist 2026: Build with context. Ship with confidence.** (Đã được người dùng phê duyệt ý tưởng):
- **Tên sản phẩm**: MedTrace GxP Compliance Guardian (Apps for Specialized Industries)
- **Mô tả**: MedTrace GxP Compliance Guardian (Apps for Specialized Industries): Hệ thống tự động kiểm toán truy xuất nguồn gốc (Traceability Matrix) chuẩn FDA 21 CFR Part 11 & ISO 13485 dành cho đội ngũ phần mềm y tế/dược phẩm: liên kết yêu cầu thiết kế trên Confluence, đánh giá rủi ro FMEA và bằng chứng kiểm thử trên Jira qua Forge + Rovo Agent để xuất hồ sơ thẩm định kiểm toán chỉ trong 1 click.
- **Góc độ thắng giải**: Đánh vào hạng mục ít cạnh tranh nhất là Apps for Specialized Industries ($15k), giải quyết nỗi đau kiểm toán pháp lý cực đắt đỏ trong ngành y tế/sinh học thay vì các công cụ dev thông thường.
- **Quy trình kỹ thuật**: **SDD → VSDD → CoDD** của `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`.

## Architectural decisions (đọc trước khi sửa)

| Quyết định | Lý do | Ngày |
|---|---|---|
| Chốt ý tưởng `MedTrace GxP Compliance Guardian (Apps for Specialized Industries)` | Đã qua bước Human Approval Gate trước khi build | 2026-10 |
| Áp dụng Studio Harness (`SDD → VSDD → CoDD`) | Đảm bảo mọi tính năng đều có `DESIGN.md`, `SPEC.md` (`AC-1..N`), test tự động và `VALIDATION.md` | 2026-10 |

## Known gaps (đừng "sửa nhầm")

- Chưa có (cập nhật trong quá trình chạy `/build` và `/validate`).

## Structure aliases (SPEC ↔ code)

- `SPEC.md` → Đặc tả hệ thống & danh sách `- AC-1: ...`
- `DESIGN.md` → Hệ thống thiết kế UI/UX
- `VALIDATION.md` → Báo cáo nghiệm thu theo chuẩn Studio Harness
- `SUBMISSION.md` → Bài thuyết trình nộp Devpost
