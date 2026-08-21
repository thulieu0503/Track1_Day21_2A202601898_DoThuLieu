# K3 Track 1 Day 20-21 - AI Evaluation Capstone

## Thong tin

- Ho ten: Đỗ Thu Liễu
- Nhom: Phạm Tiến Đại, Nguyễn Trí Trung, Đỗ Thu Liễu
- Case: VLearn AI Tutor
- Ngay xac nhan: 2026-08-21

## Dong gop cua toi

- Doc 5 case `quote_verbatim` con fail sau nhieu vong sua prompt/retry (v3-v5), tu
  doi chieu voi file corpus goc thay vi doan.
- Phat hien goc re chung: slide/bang nhieu cot trong corpus (`slide-day19-20`,
  bang pandoc trong `anthropic-demystifying-evals.md`) bi cong cu convert
  PDF->markdown lam phang, khong phai loi model.
- Chon huong sua `load_corpus()` (rui ro cao hon, anh huong retrieval toan corpus)
  thay vi dung o backlog - dua `quote_verbatim` tu 73% len 88% (95,8% tren dong
  hop le).
- Tu choi de AI "cham gia" ket qua nhan nguoi cho bai dep hon; giu verdict CHUA
  TRIEN KHAI dung so that du rat gan nguong.

## Verdict tom tat

**CHUA TRIEN KHAI** - `quote_verbatim` v6 dat 88% (23/26, 95,8% tren 24 dong hop
le), tang tu 19% (v1) qua 6 vong sua nhung van chua dat nguong chan "gan 100%"
nhom da tu dat va xac nhan o REPORT.md muc 6.

## File chinh

- `deliverables/REPORT.md`: bao cao 7 muc va verdict cuoi.
- `deliverables/ai-support-log.md`: nhat ky dung AI, co phan rieng cho tung thanh vien.
- `deliverables/evidence/`: data tho cua dataset, results (v1-v6), labels, judge
  prompts, verdicts va code checks.
- `deliverables/evidence/labels-v3.csv`: spot-check 1 nguoi export tu `report.html`
  cho `results-v3.jsonl` (hanh vi grounded/scope khong doi giua v3-v6).
