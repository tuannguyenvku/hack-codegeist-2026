---
name: studio-harness
description: Hệ thống Agent & Skill chuẩn SDD -> VSDD -> CoDD từ AgentAppStudio Studio Harness (/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness) dùng để thiết kế (DESIGN.md), đặc tả (SPEC.md), lập trình theo tiêu chí nghiệm thu (AC-*), kiểm thử và nghiệm thu (VALIDATION.md).
---

# Studio Harness Integration (/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness)

Dự án này sử dụng trực tiếp các Agent roles (`Product`, `Architecture`, `Engineering`, `Review`, `QA`, `Release`) và bộ kỹ năng trong `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness`:

- **Quy trình bắt buộc**: `SDD (Spec-Driven) -> VSDD (Verified Spec-Driven) -> CoDD (Constraint-Driven)`
- **Các quy trình kỹ năng đã được gắn vào `.claude/commands/`**:
  - Thiết kế hệ thống giao diện: `.claude/commands/design-init.md` -> xuất `DESIGN.md`
  - Đặc tả kỹ thuật & tiêu chí nghiệm thu: `.claude/commands/spec.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/SPEC.md`) -> xuất `SPEC.md` (chứa các dòng `- AC-1: ...`, `- AC-2: ...`)
  - Kiểm tra độ phủ tiêu chí SPEC: `npm --prefix /Volumes/AllySSD/Projects/AgentAppStudio/studio-harness run coverage:check -- --spec ./SPEC.md`
  - Lập trình theo vòng lặp Red-Green-Verify: `.claude/commands/build.md`
  - Nghiệm thu độc lập & CTO Review: `.claude/commands/validate.md` & `.claude/commands/cto.md` (theo mẫu `/Volumes/AllySSD/Projects/AgentAppStudio/studio-harness/templates/VALIDATION.md`) -> xuất `VALIDATION.md`
