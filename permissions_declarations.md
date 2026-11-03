# Permission Declarations — Live TV: M3U Player (05j)

Package: `com.m3uplay.livetv.player` · targetSdk: **36**

## Kết luận

**KHÔNG CÓ permission nhạy cảm cần declaration trên Play Console.**

App không sử dụng bất kỳ API/permission nhạy cảm nào thuộc danh sách cần khai báo:
- Không Accessibility Service
- Không Draw Over Other Apps (SYSTEM_ALERT_WINDOW)
- Không Usage Stats (PACKAGE_USAGE_STATS)
- Không Notification Listener
- Không VPN Service
- Không Device Admin
- Không QUERY_ALL_PACKAGES
- Không SMS / Call Log permissions
- Không Background Location
- Không Foreground Service Type
- Không Camera / Microphone
- Không READ_CONTACTS, ACCESS_FINE_LOCATION, READ_MEDIA_*

## Permissions có trong manifest (không cần declaration)

| Permission | Lý do | Declaration cần? |
|---|---|---|
| `INTERNET` | Fetch M3U playlists + stream media | Không |
| `ACCESS_NETWORK_STATE` | Kiểm tra kết nối trước khi fetch | Không |
| `ACCESS_WIFI_STATE` | Kiểm tra loại mạng | Không |
| `AD_ID` | Advertising ID cho AdMob/mediation | Không (khai trong Data Safety) |
| `ACCESS_ADSERVICES_AD_ID` | Android 13+ Ad Services | Không |
| `ACCESS_ADSERVICES_ATTRIBUTION` | Attribution API | Không |
| `BILLING` | Template từ module-ads (ad-free flag) — KHÔNG có IAP thật | Không |
| `POST_NOTIFICATIONS` | Android 13+ opt-in notification | Không (standard permission) |

## Video demo

**KHÔNG CẦN.** Không có permission nhạy cảm → không cần quay video demo cho Play Console.

## Ghi chú targetSdk 36

targetSdk = 36 chưa bắt buộc minimize permissions theo policy 16909972 (hiệu lực 27/01/2027 cho targetSdk ≥ 37).
App không dùng READ_CONTACTS, ACCESS_FINE_LOCATION, READ_MEDIA_* nên không cần chuẩn bị justification.
