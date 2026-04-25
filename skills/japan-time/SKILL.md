---
name: japan-time
description: Return the current time in Japan (JST, Asia/Tokyo) whenever the user asks for Japanese time, Tokyo time, or mentions “日本时间/日本時間/JST/东京时间/東京時間”. Use this skill to provide accurate real-time Japan time with explicit date, weekday, and timezone.
---

# Japan Time Command Skill

Use this skill when the user asks for current Japan time.

## Steps

1. Run this command to fetch current JST time:

```bash
TZ=Asia/Tokyo date '+%Y-%m-%d %H:%M:%S (%A) JST (UTC%z)'
```

2. Reply with the exact returned value.
3. If helpful, include equivalent UTC time by running:

```bash
date -u '+%Y-%m-%d %H:%M:%S UTC'
```

## Notes

- Always use `Asia/Tokyo` timezone explicitly.
- Japan does not use daylight saving time.
- Prefer 24-hour format.
