# internship-2026
Chương trình học việc React Web Developer 2026
# Tổng kết học việc — Nguyễn Hải Đăng
 
## Em đã học được gì
 
- **Optimistic update đúng flow:** Trước đây em không biết `onMutate` snapshot là gì — cứ nghĩ gọi `setQueryData` rồi `invalidateQueries` là xong. Giờ em hiểu tại sao cần rollback: nếu API lỗi mà không có snapshot thì UI sẽ hiển thị sai mãi mãi.
- **TanStack Query cache hoạt động thế nào:** Phân biệt được `staleTime` (bao lâu thì coi là cũ) vs `gcTime` (bao lâu thì xóa khỏi bộ nhớ), và khi nào dùng `setQueryData` thay vì `invalidateQueries`.
- **TypeScript thực dụng hơn:** Biết dùng `Omit`, `Pick`, `Partial` thay vì viết lại type thủ công. Đặc biệt học được `satisfies` — dùng thay type assertion trong optimistic update để an toàn hơn.
- **URL state sync:** Trước đây em lưu filter/search trong `useState`, không biết đây là anti-pattern. Giờ hiểu tại sao phải sync lên URL và cách tách thành custom hook `useTableQueryState` xử lý cả edge case param không hợp lệ.
- **Testing có chủ đích:** Biết ưu tiên `getByRole` hơn `getByTestId`, dùng `vi.useFakeTimers()` để test debounce, và hiểu thế nào là "test behavior, không test implementation".
- **Git workflow chuẩn:** Từ task COM-79 trở đi em mới thực sự dùng conventional commits và biết interactive rebase để làm sạch history trước khi mở PR.
- **Framework Next.js:** Hiểu hơn và đã có thể sử dụng Next.js để xây dựng ứng dụng.
- **Kiến thức nền của React:** React Fundamentals, React Hooks, React Hook Form + Zod, Zustand .
- **Xây dựng layout, kết hợp Tailwind + Shadcn UI:**
## Điểm em thấy bản thân tiến bộ rõ nhất
 
**1. Kiến trúc component rõ hơn hẳn.** Trước đây em viết logic thẳng vào component, lặp code ở nhiều chỗ. Sau Sprint 3–4, em đã biết tách `<ConfirmDialog>`, `<EmptyState>` thành reusable component, tách logic URL sync thành hook riêng — mentor đánh giá architecture bài test cuối "sạch".
 
**2. Optimistic update từ sai thành đúng hoàn toàn.** Bài test đầu vào em implement thiếu snapshot và không rollback. Bài test cuối kỳ, cả 3 mutations đều đúng flow 4 bước, `useUpdateUser` còn cập nhật cả 2 caches (list + detail) — được mentor khen là "rất tốt, không được yêu cầu mà vẫn làm".
 
**3. Khả năng xây dựng và đọc hiểu code, kiến thức base tốt hơn trước nhiều.** 
 
## Điểm em vẫn còn yếu và kế hoạch cải thiện
 
- **Chú ý không đều:** Hay bỏ sót chi tiết nhỏ — text thiếu dấu tiếng Việt, button thừa trong dialog, hook có sẵn nhưng chưa wire up UI. Kế hoạch: trước khi nộp bài, chạy lại checklist từ đầu thay vì chỉ nhìn vào phần vừa làm.
- **Dùng `eslint-disable` như một lối tắt:** 
- **Conventional commits chưa thành thói quen ngay từ đầu:** Chu trình làm việc với github cần cải thiện.
- **Cần bổ sung thêm nhiều kiến thức lập trình hơn:** Hiểu hơn về nhiều lý thuyết, thuật ngữ chuyên ngành. (React Context, race condition,...)
## Công cụ và quy trình làm việc em đã quen
 
Linear (quản lý task, Sprint), GitHub (PR workflow, conventional commits, interactive rebase), Claude (hỏi concept và debug), Vitest + React Testing Library, React DevTools Profiler, PR description theo template What / Why / How to test.
 
## Những gì em muốn học tiếp trong giai đoạn thử việc
 
- Hiểu codebase Babrik thực tế: data flow, cách module Wireframe render canvas, state management đang dùng
- Học cách đọc và review code người khác — em chưa có kinh nghiệm comment PR có giá trị
- Xử lý real-time hoặc collaborative editing nếu Babrik có WebSocket/CRDT
- Hiểu quy trình deploy và CI/CD của team
- Học thêm được nhiều thuật ngữ và kiến thức nâng cao hơn
