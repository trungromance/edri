# VIỆN NGHIÊN CỨU VÀ PHÁT TRIỂN DOANH NHÂN VIỆT NAM - ASEAN (EDRI)
## KIẾN TRÚC CÔNG NGHỆ TỔNG THỂ & THIẾT KẾ HỆ THỐNG MỞ RỘNG (2026 - 2029)
### TÍCH HỢP TOÀN DIỆN: CRM/CDP ĐỊNH LƯỢNG, LMS ĐÀO TẠO, MOBILE APP & HỆ THỐNG CLB - GIẢI ĐẤU THỂ THAO
*Phiên bản: 2.1 - Nâng cấp phân hệ Văn Hóa, CLB & Tournament Engine*

---

## 1. NGUYÊN TẮC THIẾT KẾ HỆ THỐNG: KIẾN TRÚC MỞ RỘNG ĐA TẦNG (COMPOSABLE SCALE-UP)

Kiến trúc công nghệ EDRI được thiết kế để **giải quyết bài toán trước mắt với chi phí 0 Đồng** nhưng sở hữu nền tảng chuẩn mực để **mở rộng thành hệ thống khổng lồ sau 2 - 3 năm** mà không cần đập đi xây lại:

1. **API-First & Headless:** Toàn bộ dữ liệu nằm tập trung tại cơ sở dữ liệu PostgreSQL (Supabase), mọi giao diện (Website, Cổng Intake, Cổng Giải Đấu Thể Thao, Mobile App, Hệ thống LMS) đều kết nối thông qua RESTful và GraphQL APIs chuẩn hóa.
2. **AI-Native Microservices:** Tích hợp trực tiếp các mô hình AI thế hệ mới (Gemini 1.5 Flash, DeepSeek, Claude) phục vụ tự động hóa sản xuất nội dung cho Ban Truyền thông và phân tích dữ liệu cho Ban Đối tác.
3. **Phân tích định lượng & Điểm gắn kết văn hóa (Cultural & Quantitative Intelligence):** Đo lường sức khỏe doanh nghiệp ($ARI$) kết hợp theo dõi mức độ tương tác thông qua các giải đấu thể thao, câu lạc bộ sở thích (Golf, Pickleball, Văn hóa doanh nhân).

---

## 2. BẢN ĐỒ HỆ SINH THÁI CÔNG NGHỆ 3 NĂM (2026 - 2029)

```
+------------------------------------------------------------------------------------------------------------------+
|                            ĐIỂM CHẠM TRẢI NGHIỆM ĐA NỀN TẢNG (OMNICHANNEL TOUCHPOINTS)                           |
|  [NĂM 1: KHỞI TẠO]               [NĂM 2: VĂN HÓA & ĐÀO TẠO]                [NĂM 3: HỆ SINH THÁI DOANH NHÂN]       |
|  - Website Portal EDRI           - Cổng Quản Trị CLB Doanh Nhân            - Mobile App EDRI (iOS & Android)       |
|  - Cổng Ghi Nhận DN (Intake)     - Hệ Thống Tổ Chức Giải Đấu Thể Thao      - Mạng xã hội doanh nhân tinh hoa       |
|  - Zalo Mini App / QR Check-in   - Nền tảng Đào tạo LMS Hybrid             - Sàn giao thương B2B ASEAN trực tuyến  |
+------------------------------------------------------------------------------------------------------------------+
                                                        │
                                                        ▼
+------------------------------------------------------------------------------------------------------------------+
|                            TẦNG ĐIỀU PHỐI VÀ AN NINH (EDGE GATEWAY & COMPLIANCE)                                 |
|         Cloudflare Enterprise CDN / WAF / SSL  <=====>  Role-Based Access Control (RBAC) & OAuth2               |
|         Tuân thủ nghiêm ngặt Nghị định 13/2023/NĐ-CP về bảo vệ dữ liệu cá nhân & thông tin doanh nghiệp         |
+------------------------------------------------------------------------------------------------------------------+
                                                        │
                                                        ▼
+------------------------------------------------------------------------------------------------------------------+
|                            CÁC KHỐI NỀN TẢNG PHỤC VỤ TỪNG PHÒNG BAN CHỨC NĂNG                                    |
|                                                                                                                  |
|  [BAN VĂN HÓA, THỂ THAO & CÂU LẠC BỘ]        [BAN PHÁT TRIỂN ĐỐI TÁC DN VN & QUỐC TẾ]                            |
|  - Club Management Portal: Điểm danh CLB     - CRM Quản trị mạng lưới đối tác ngoại giao & DN                    |
|  - Tournament Engine: Xếp bảng & Live Score  - Nền tảng Phân tích Định lượng (Quantitative Analytics)            |
|  - Sponsorship Digital Hub: Số hóa tài trợ   - Thuật toán AI Matchmaking ghép đôi B2B tự động                    |
|                                                                                                                  |
|  [BAN TRUYỀN THÔNG & THƯƠNG HIỆU]            [BAN ĐÀO TẠO & HỌC VIỆN DOANH NHÂN]                                 |
|  - AI Content Studio (Bài viết, video)       - Hệ thống LMS Hybrid (Offline & Online)                            |
|  - Truyền thông giải đấu thể thao đa kênh    - Quản lý học viên, khảo sát & Chứng chỉ số QR                      |
|                                                                                                                  |
|  [VĂN PHÒNG VIỆN & BAN LÃNH ĐẠO]                                                                                 |
|  - Executive War Room Dashboard (Báo cáo hội viên, doanh thu tài trợ giải đấu, giao thương ASEAN thời gian thực)  |
+------------------------------------------------------------------------------------------------------------------+
                                                        │
                                                        ▼
+------------------------------------------------------------------------------------------------------------------+
|                            HẠ TẦNG DỮ LIỆU & TRÍ TUỆ NHÂN TẠO (DATA & AI ENGINE)                                 |
|  - CDP Hồ sơ 360°: Định danh, Năng lực SME, Điểm gắn kết Văn hóa/Thể thao, Thị trường mục tiêu ASEAN             |
|  - Cơ sở dữ liệu quan hệ PostgreSQL (Supabase Backend) + Lưu trữ tài liệu đám mây (Cloudflare R2)                |
+------------------------------------------------------------------------------------------------------------------+
```

---

## 3. THIẾT KẾ CÔNG NGHỆ PHÂN HỆ VĂN HÓA, CLB & TỔ CHỨC GIẢI ĐẤU

### 3.1. Cổng Quản Trị Mạng Lưới Câu Lạc Bộ Doanh Nhân (Club Portal)
- **Mục tiêu:** Quản lý sinh hoạt các CLB chuyên đề của Viện: CLB Golf Doanh nhân ASEAN, CLB Pickleball Doanh nhân, CLB Tennis, CLB Chạy bộ kết nối, CLB Nữ Doanh nhân, CLB Văn hóa - Nghệ thuật Doanh nhân.
- **Tính năng số hóa:**
  - Danh bạ thành viên theo từng CLB, quản lý Ban Chủ nhiệm CLB.
  - Lịch sinh hoạt định kỳ, thông báo tự động qua Zalo OA/Email.
  - Điểm danh thông minh qua mã QR tại mỗi buổi sinh hoạt.
  - Điểm tích lũy gắn kết thành viên (Loyalty & Engagement Points).

### 3.2. Hệ Thống Tổ Chức Giải Đấu Thể Thao Số Hóa (Tournament & League Engine)
- **Cổng đăng ký giải đấu trực tuyến (Registration Gateway):**
  - Đăng ký theo cá nhân hoặc đoàn thể doanh nghiệp.
  - Chọn bảng thi đấu (Bảng A, B, C theo Handicap Golf, hoặc các hạng mục Đôi nam, Đôi nữ, Đôi nam nữ Pickleball/Tennis).
  - Tải lên ảnh vận động viên và giấy xác nhận doanh nghiệp.
- **Thuật toán chia bảng & xếp lịch tự động (Bracket Engine):**
  - Tự động sinh lịch thi đấu theo thể thức đấu vòng tròn hoặc loại trực tiếp.
  - Điều phối sân đấu và khung giờ tránh trùng lặp.
- **Bảng điểm trực tuyến thời gian thực (Live Leaderboard):**
  - Trọng tài cập nhật tỷ số trực tiếp trên điện thoại di động (Mobile Referee App).
  - Bảng tỷ số cập nhật tức thời (Live Score) hiển thị trên màn hình LED sân đấu và trang web giải đấu cho khán giả/cổ động viên theo dõi từ xa.
- **Cổng Số Hóa Quyền Lợi Tài Trợ (Sponsorship Digital Hub):**
  - Hiển thị vị trí nhà tài trợ: Kim Cương, Vàng, Bạc, Đồng trên bảng tỷ số và livestream.
  - Gian hàng số giới thiệu sản phẩm của doanh nghiệp tài trợ.
  - Thống kê lượt tiếp cận thương hiệu để báo cáo hiệu quả cho nhà tài trợ.

---

## 4. BỔ SUNG SCHEMA CƠ SỞ DỮ LIỆU CLB & GIẢI ĐẤU (POSTGRESQL / SUPABASE)

```sql
-- 1. Bảng Câu Lạc Bộ Doanh Nhân (Clubs)
CREATE TABLE edri_clubs (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    club_name VARCHAR(255) NOT NULL, -- CLB Golf Doanh nhân ASEAN, CLB Pickleball...
    category VARCHAR(50) NOT NULL, -- SPORTS_GOLF, SPORTS_PICKLEBALL, CULTURE_ART, WOMEN_LEADERS
    leader_entrepreneur_id UUID REFERENCES edri_entrepreneurs(id),
    description TEXT,
    logo_url TEXT,
    is_active BOOLEAN DEFAULT TRUE,
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- 2. Bảng Thành Viên CLB (Club Memberships)
CREATE TABLE edri_club_members (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    club_id UUID REFERENCES edri_clubs(id) ON DELETE CASCADE,
    entrepreneur_id UUID REFERENCES edri_entrepreneurs(id) ON DELETE CASCADE,
    role VARCHAR(50) DEFAULT 'MEMBER', -- PRESIDENT, VICE_PRESIDENT, MEMBER
    handicap_or_level VARCHAR(50), -- Handicap golf hoặc trình độ pickleball
    joined_date DATE DEFAULT CURRENT_DATE,
    is_active BOOLEAN DEFAULT TRUE
);

-- 3. Bảng Giải Đấu Thể Thao & Sự Kiện Văn Hóa (Tournaments)
CREATE TABLE edri_tournaments (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    title VARCHAR(255) NOT NULL, -- Giải Golf Hữu Nghị Việt Nam - ASEAN Cúp EDRI 2027
    sport_type VARCHAR(50) NOT NULL, -- GOLF, PICKLEBALL, TENNIS, RUNNING
    start_date DATE NOT NULL,
    end_date DATE NOT NULL,
    venue TEXT NOT NULL, -- Sân Golf Long Biên, Sân Thể Thao EDRI...
    status VARCHAR(50) DEFAULT 'UPCOMING', -- UPCOMING, ONGOING, COMPLETED
    banner_url TEXT,
    total_slots INT DEFAULT 144,
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- 4. Bảng Vận Động Viên & Đội Thi Đấu (Tournament Participants)
CREATE TABLE edri_tournament_participants (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    tournament_id UUID REFERENCES edri_tournaments(id) ON DELETE CASCADE,
    enterprise_id UUID REFERENCES edri_enterprises(id),
    entrepreneur_id UUID REFERENCES edri_entrepreneurs(id),
    division VARCHAR(50), -- Bảng A, Bảng B, Đôi nam...
    score_summary VARCHAR(100),
    rank_position INT,
    registered_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);

-- 5. Bảng Nhà Tài Trợ Giải Đấu (Tournament Sponsors)
CREATE TABLE edri_tournament_sponsors (
    id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
    tournament_id UUID REFERENCES edri_tournaments(id) ON DELETE CASCADE,
    enterprise_id UUID REFERENCES edri_enterprises(id) ON DELETE CASCADE,
    tier VARCHAR(50) NOT NULL, -- DIAMOND, GOLD, SILVER, CO_SPONSOR
    contribution_amount NUMERIC(15,2),
    logo_url TEXT,
    booth_url TEXT,
    created_at TIMESTAMP WITH TIME ZONE DEFAULT NOW()
);
```
