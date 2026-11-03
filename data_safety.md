# Data Safety Audit — Live TV: M3U Player (05j)

Package: `com.m3uplay.livetv.player` · Generated: 2026-11-03

## Tóm tắt khai báo

| Mục | Giá trị |
|---|---|
| Thu thập dữ liệu? | **Có** |
| Mã hoá truyền tải? | **Có** (HTTPS; cleartext chỉ cho M3U streams — user data qua HTTPS) |
| Tài khoản? | **Không** — app không cho tạo/đăng nhập tài khoản |
| Xoá dữ liệu? | Tự động xoá trong 90 ngày (SDK analytics/attribution) |
| Đã review bảo mật độc lập? | Không |

## Data types khai báo

### Thu thập (Collected only — KHÔNG shared)

| Data type | SDK nguồn | Mục đích | Bắt buộc? |
|---|---|---|---|
| Crash logs | Firebase Crashlytics | App functionality | Có |
| Diagnostics | Firebase Analytics + Crashlytics | Analytics | Có |
| App interactions | Firebase Analytics | Analytics | Có |

### Thu thập VÀ chia sẻ (Collected + Shared)

| Data type | SDK nguồn | Mục đích thu thập | Mục đích chia sẻ | Bắt buộc? |
|---|---|---|---|---|
| Device or other IDs | AdMob, Adjust, Facebook SDK, TikTok SDK | Advertising | Advertising | Có |

### KHÔNG thu thập (xác nhận)

- Personal info: name, email, user IDs, address, phone, race/ethnicity, political/religious beliefs, sexual orientation, other
- Financial: payment info, purchase history, credit score, other
- Location: approximate, precise
- Web browsing history
- Messages: email, SMS, in-app
- Photos and videos
- Audio files
- Health and fitness
- Contacts
- Calendar
- Files and docs
- App activity: in-app search, installed apps, user-generated content, other actions

## Căn cứ

1. **compliance_census.md** — kiểm kê SDK: Firebase Analytics/Crashlytics/RC, AdMob/mediation (module-ads), Adjust, Facebook SDK, TikTok SDK
2. Không account/login → không user ID, không email, không name
3. Playlists/favorites/history = DataStore local, không rời thiết bị
4. `POST_NOTIFICATIONS` = opt-in standard, không nhạy cảm
5. `AD_ID` permission → Device IDs shared cho advertising
6. Không IAP thật (BILLING từ module-ads template)

## File CSV

`data_safety.csv` — import trực tiếp vào Play Console (App content → Data safety → Import).
