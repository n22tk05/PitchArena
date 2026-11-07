# PITCH·ARENA STUDIO // ĐẤU TRƯỜNG PHẢN BIỆN GIẢ LẬP

> **AI REALTIME VOICE DEFENSE SIMULATOR // POWERED BY GEMINI 2.5 FLASH**  
> Tôi Luyện Bản Lĩnh Đối Chất Trước Giờ G Hội Đồng. Mô phỏng áp lực phòng thi thật qua đối thoại giọng nói trực tiếp 220ms với 4 Giám khảo AI Solo Bosses. Bóc tách lỗ hổng đề tài, bắt bẫy ngụy biện và tự động xuất bản Cẩm nang phản đòn 3 cột chi tiết.

---

## 🕹️ Tổng Quan Dự Án

**PITCH·ARENA** là nền tảng đấu trường phản biện giả lập chuyên sâu dành cho sinh viên và các nhà sáng lập khởi nghiệp chuẩn bị bước vào vòng thi thuyết trình & hỏi đáp (Q&A) trước Hội đồng Giám khảo chuyên nghiệp (SV-Startup, Euréka, Hult Prize, Hackathon, Hội đồng NCKH).

Hệ thống kết hợp công nghệ **In-Memory GraphRAG** bóc tách văn bản đề án thông minh (loại bỏ hình ảnh rác, lập bảng số liệu Entity Whitelist chống ảo giác 99.4%) cùng mô hình **Voice-in / Text-out Streaming** phản hồi dưới 1.0 giây, biến những bài tập dượt đơn điệu thành các phiên tranh biện đối kháng nảy lửa 24/7.

### 🎨 Phong Cách Thiết Kế: *Warm Bronze & Sand Studio Design System*
- **Bảng màu ấm áp & Chuyên nghiệp**: Nền cát ấm `#FAF8F5`, thẻ làm việc `#FFFFFF`, sắc đồng cổ điển `#B45309`, `#D97706` và điểm nhấn vàng ánh kim `#FEF3C7`.
- **Bộ phông chữ thống nhất**: Font chữ hiện đại `Plus Jakarta Sans` chuẩn công thái học kết hợp điểm xuyết pixel retro `Press Start 2P`.
- **Phản hồi xúc giác (Tactile Micro-interactions)**: Đổ bóng cơ học nhẹ (`shadow-xs`), hiệu ứng nhấn nút tactile máy thùng game arcade (`active:translate-x-0.5`).
- **Telemetry thời gian thực**: Đo lường nhịp nói (WPM), phát hiện khoảng lặng nhịp thở (VAD > 2.0s), chỉ báo âm lượng Vocal Band và sóng âm Audio Waveform trực quan.

---

## ⚡ Quy Trình 5 Giai Đoạn Khép Kín (5-Stage Studio Architecture)

Hệ thống mô phỏng trọn vẹn chu trình 5 bước của một buổi bảo vệ đề án từ lúc nạp bài đến khi nhận cẩm nang phản đòn:

```
[ BƯỚC 01 ] ──► [ BƯỚC 02 ] ──► [ BƯỚC 03 ] ──► [ BƯỚC 04 ] ──► [ BƯỚC 05 ]
Nạp Đề Tài      Cấu Hình Sảnh   Pitch Stage      Combat Arena    Báo Cáo Phụ Lục
In-Memory RAG   Lobby & Voice   Thuyết Trình     4 Bosses Q&A    Ma Trận 3 Cột
+ Tải Tệp Mẫu   Testing Lab     WPM Telemetry    Thanh Máu HP    + Slide 48H
```

### 1. Bước 01: Nạp Dữ Liệu & In-Memory GraphRAG
- Tiếp nhận tệp thuyết minh đề tài Microsoft Word (`.docx`, dung lượng tối đa 20MB).
- Tự động bóc tách **5 khối kinh doanh trọng yếu**:
  1. *Executive Summary & Problem Statement* (Tổng quan & Vấn đề thị trường)
  2. *Market Opportunity & Target Customer* (Quy mô thị trường & Khách hàng mục tiêu)
  3. *Product Architecture & Tech Innovation* (Kiến trúc sản phẩm & Đổi mới công nghệ)
  4. *Business Model & Unit Economics* (Mô hình kinh doanh, CAC, LTV, Biên lợi nhuận)
  5. *Execution Roadmap & Financial Projections* (Lộ trình triển khai & Dự phóng tài chính)
- Tự động nhận diện **3 điểm mù rủi ro** trước hội đồng.
- **Thử nghiệm tức thì & Tải tệp mẫu**:
  - Bấm `[ DÙNG ĐỀ TÀI MẪU ]` để nạp ngay hồ sơ MedTech AI mẫu.
  - Bấm `[ TẢI TÀI LIỆU MẪU (.DOCX) ]` để tải file `Thuyet_Minh_De_Tai_AI_Medical_Assistant.docx` chuẩn 5 khối về máy tính tham khảo.

### 2. Bước 02: Thiết Lập Phòng Đấu & Giám Khảo (Lobby Config)
- Tùy chỉnh mức độ khắt khe và độ khó của Hội đồng Giám khảo (Thử thách, Tiêu chuẩn, Tập dượt).
- Lựa chọn đấu với toàn thể Hội đồng 4 Giám khảo hoặc chọn Solo Boss chuyên sâu.
- **Microphone Testing Lab**: Kiểm tra thiết bị thu âm, kiểm tra dải tần giọng nói Vocal Band (100Hz – 4000Hz) và độ nhạy trước khi vào trận.

### 3. Bước 03: Thuyết Trình Đề Tài Trực Tiếp (Pitch Stage)
- Trình bày trực tiếp qua micro với streaming Speech-to-Text (STT) thời gian thực.
- Phân tích tốc độ nói (WPM – Words Per Minute) qua cửa sổ trượt Rolling Window, cảnh báo khi nói quá nhanh (> 180 WPM) hoặc quá chậm (< 100 WPM).
- Thuật toán VAD (Voice Activity Detection) phát hiện khoảng lặng nhịp thở.
- Hỗ trợ chuyển đổi linh hoạt giữa chế độ **Nói qua Micro** và **Gõ bàn phím**.

### 4. Bước 04: Đấu Trường Tranh Biện Trực Diện (Combat Arena)
- Cơ chế chất vấn dồn dập với **Bộ tứ Giám khảo Khắc nghiệt (4 Jury Bosses)**:
  - 🦈 **Shark Trần Nam** *(Market Shark)*: Săn lùng bằng chứng trả tiền thực tế, bóc trần khảo sát thái độ ảo, xoáy sâu CAC, LTV và kênh tiếp cận 100 khách hàng đầu tiên.
  - 🤖 **TS. Lê Minh Trang** *(AI Sentinel)*: Thẩm định kiến trúc kỹ thuật, độ trễ API, giải pháp xử lý ngoại lệ khi mất mạng và nguy cơ bị đối thủ copy.
  - 🔥 **GS. Vũ Hoàng** *(Finance Dragon)*: Truy vấn dòng tiền 6 tháng đầu, chi phí OpEx, điểm hòa vốn (break-even) và cơ chế tự chủ tài chính không dựa vào tài trợ.
  - 🛡️ **ThS. Đặng Mai Lan** *(Risk Strategist)*: Bóc trần rào cản phòng thủ (Moat), rủi ro pháp lý, quyền sở hữu trí tuệ và tính kỷ luật trong lộ trình phân công KPI.
- **Quy tắc thi đấu sống còn**:
  - Đồng hồ áp lực **30 - 45 giây/lượt** phản biện.
  - **Thanh sinh lực luận điểm (Defense Health Bar)**: Trừ máu (-10% đến -25% HP) khi trả lời vòng vo, né tránh hoặc dính bẫy ngụy biện logic; hồi phục khi dẫn chứng số liệu thực tế.
  - **Phao cứu sinh Strike 2 (Panic Freeze 30s)**: Đóng băng thời gian 30 giây để hội ý và nhận gợi ý gỡ điểm từ chế độ sư phạm.

### 5. Bước 05: Báo Cáo Phụ Lục Chiến Thuật (Diagnostic Report & Actionable Matrix)
- **Biểu đồ biến thiên HP (HpTimelineChart)**: Trực quan hóa toàn bộ thăng trầm của điểm số qua từng lượt chất vấn.
- **Bảng đối soát 3 cột (Actionable Matrix)**:
  - *Cột 1*: Câu hỏi Giám khảo & Ý đồ thẩm định cốt lõi (Jury Intent).
  - *Cột 2*: Lỗ hổng bị bóc trần, bẫy ngụy biện và điểm gãy logic.
  - *Cột 3*: Đề xuất chỉnh sửa Slide, **Cấu trúc 3 khối cần vẽ lên Slide phụ lục (Slide Skeleton 48H)**, **3 bước hành động cụ thể trong 48H** và **Câu trả lời chuẩn mực (Winning Response)** có nút bấm sao chép tức thì.
- **Xuất báo cáo & Tái đấu**: Tải báo cáo chi tiết định dạng Markdown (`.md`) về máy tính và chọn `[ TÁI ĐẤU (REMATCH) ]` để lập tức cải thiện điểm số.

---

## 🛠️ Kiến Trúc Kỹ Thuật (Tech Stack)

Dự án được xây dựng theo mô hình **Monorepo (npm workspaces)**:

```
TS/
├── packages/
│   └── shared/               # Thư viện dùng chung TypeScript interfaces, types & Zod schemas
├── server/                   # Backend API NestJS 10, WebSocket Gateway & In-Memory RAG Engine
├── client/                   # Frontend SPA React 18, Vite 5, Tailwind CSS 3, Lucide Icons
│   └── public/
│       └── samples/          # File Word đề tài mẫu .docx tải về máy tính
└── package.json              # Root workspace orchestrator
```

### Backend (`server/`)
- **Framework**: [NestJS 10](https://nestjs.com/) (Module, Controller, Service, Gateway architecture).
- **Realtime WebSocket**: [Socket.IO](https://socket.io/) (kết nối 2 chiều độ trễ thấp 220ms cho phòng đấu Arena).
- **Document Processing**: [Mammoth.js](https://github.com/mwilliamson/mammoth.js) (bóc tách clean text từ `.docx`, tự động lọc bỏ ảnh chụp màn hình rác).
- **Entity Extraction**: [Vercel AI SDK](https://sdk.vercel.ai/) (`ai`, `@ai-sdk/google`) tích hợp Google Gemini 2.5 Flash / 2.0 Flash.
- **File Upload**: Multer (In-memory storage buffer, xử lý trực tiếp trên RAM, không lưu đĩa, bảo mật tối đa).
- **Validation**: Zod + class-validator.

### Frontend (`client/`)
- **Framework**: [React 18](https://react.dev/) + [Vite 5](https://vitejs.dev/).
- **Styling**: [Tailwind CSS 3](https://tailwindcss.com/) + Custom Retro Keyframes (`index.css`).
- **Typography**: `Plus Jakarta Sans` kết hợp `Press Start 2P`.
- **Speech Recognition**: Web Speech API kết hợp cơ chế tích lũy chuỗi chống lặp câu và bộ lọc tiếng Việt.
- **Icons**: [Lucide React](https://lucide.dev/).
- **Networking**: Axios Client + Socket.IO Client.

---

## 🚀 Hướng Dẫn Cài Đặt & Chạy Dự Án

### 1. Yêu Cầu Môi Trường
- **Node.js**: Phiên bản `>= 18.x` (khuyến nghị 20.x LTS)
- **npm**: Phiên bản `>= 9.x`

### 2. Cài Đặt Dependencies
Từ thư mục gốc của dự án:
```bash
npm install
```

### 3. Cấu Hình Biến Môi Trường (.env)

#### Backend (`server/.env`):
Tạo tệp `server/.env` với nội dung:
```env
PORT=4000
GEMINI_API_KEY=your_google_gemini_api_key_here
```
*(Nếu chưa có API Key Gemini, bạn có thể tạo miễn phí tại [Google AI Studio](https://aistudio.google.com/)).*

#### Frontend (`client/.env`):
Tạo tệp `client/.env` với nội dung:
```env
VITE_API_URL=http://localhost:4000
```

### 4. Khởi Chạy Ứng Dụng

#### Cách 1: Chạy song song cả Backend và Frontend (Khuyên dùng)
```bash
npm run dev
```

#### Cách 2: Khởi chạy riêng từng phần
- **Chạy NestJS Backend** (Port 4000):
  ```bash
  npm run start:dev --workspace=pitcharena-server
  ```
- **Chạy Vite Frontend** (Port 3000):
  ```bash
  npm run dev --workspace=pitcharena-client
  ```

Mở trình duyệt truy cập: **`http://localhost:3000`** để bắt đầu trải nghiệm đấu trường!

---

## 📋 Danh Sách API Endpoints Chính

| Method | Endpoint | Mô tả |
| :--- | :--- | :--- |
| `POST` | `/api/documents/upload` | Upload tệp `.docx` (multipart/form-data), chạy In-Memory RAG bóc tách 5 khối, 3 điểm mù và bảng Whitelist |
| `GET` | `/api/documents/sample/download` | Tải xuống tệp Word đề tài mẫu (`Thuyet_Minh_De_Tai_AI_Medical_Assistant.docx`) |
| `GET` | `/api/documents/health` | Kiểm tra trạng thái hoạt động của NestJS Document Service |
| `WS` | `/arena` | Kênh WebSocket thời gian thực trao đổi dữ liệu phiên đấu, đồng hồ, streaming transcript và phán quyết |

---

## 🧪 Quy Định Kiểm Tra Mã Nguồn (Critical Execution Rules)

Dự án áp dụng quy chuẩn kiểm tra chất lượng chặt chẽ:
1. **Kiểm tra kiểu dữ liệu (Typecheck)**:
   - Client: `npx tsc -p client/tsconfig.json --noEmit`
   - Server: `npx tsc -p server/tsconfig.json --noEmit`
2. **Kiểm thử tự động E2E**:
   - Chạy bộ test Playwright: `npx playwright test test/e2e/comprehensive-matrix.spec.ts`

---

## 📜 Giấy Phép & Bản Quyền

Dự án được xây dựng phục vụ nghiên cứu, đổi mới sáng tạo và huấn luyện kỹ năng phản biện khởi nghiệp cho sinh viên Việt Nam.  
**© 2026 PITCH·ARENA STUDIO — UNIVERSITY EDITION.**
