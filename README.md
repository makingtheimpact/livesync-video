# LiveSync Video Plugin

**LiveSync Video Plugin** is a powerful, lightweight WordPress plugin built for content creators and streamers who want to integrate **livestreaming status**, **live video embedding**, and a **customizable video library** directly into their WordPress sites. With built-in support for **YouTube** and **Twitch**, and a performance-first approach that minimizes API calls and caching conflicts, LiveSync makes it easy to keep your audience engaged without slowing down your site.

---

## 🎯 Target Users

- YouTubers and Twitch streamers  
- Podcasters or video content creators  
- Membership or community sites with regular live content  
- Creators using managed WordPress hosting (e.g., WP Engine, EasyWP)

---

## 🚀 Key Features

### ✅ Core Functionality

- **Livestream Status Badge**
  - Customizable location, style, color, and text
  - Auto-hides when offline
  - AJAX-loaded to avoid cache interference

- **Livestream Embed Shortcode**
  - Automatically displays the current livestream
  - Fallback display when the stream is offline
  - Support for both YouTube and Twitch live embeds

- **Video Library Display**
  - Embed latest videos from a channel or playlist
  - Filters: Most popular, recent, date range
  - Grid/list display with optional lazy loading
  - Shortcode-based output for flexible placement

- **Efficient API & Caching**
  - Uses background cron jobs to fetch updates
  - Data stored in WordPress transients
  - AJAX for livestream status to bypass full-page caching
  - Settings to configure cache expiration time

- **User-Friendly Admin UI**
  - Tabbed settings page for easy configuration
  - API key input for YouTube and Twitch
  - Color and style selectors for badge and embed layout

---

## 🧱 Planned Add-On Features (Future Versions)

- Support for additional platforms: Kick, Rumble, Facebook Live  
- Gutenberg block integration  
- Scheduled livestream countdown timer  
- Live chat embed toggle  
- Shortcodes like `[if_live]...[/if_live]` to show content only when live  
- Settings import/export  
- View analytics (optional addon)

---

## 🔐 Development Philosophy

- **Secure:** Sanitize all input, validate API data, and escape output  
- **Efficient:** Background cron jobs, minimal API calls, smart caching  
- **Compatible:** Works with managed hosts (WP Engine, EasyWP, etc.)  
- **Extensible:** Action/filter hooks for developers  
- **Cache-Safe:** AJAX-based dynamic status and cache exclusion strategies

---

## ⚙️ Technical Notes for Development

- Use `wp_schedule_event` and `wp_cron` for periodic updates  
- Store API results in `transients` or `options` with TTLs  
- Use `admin_enqueue_scripts` and `wp_enqueue_scripts` for CSS/JS  
- Separate frontend AJAX calls for livestream status (`wp_ajax` / `wp_ajax_nopriv`)  
- Provide shortcodes such as:
  - `[livesync_status]`
  - `[livesync_embed platform="youtube" channel="..."]`
  - `[livesync_library platform="youtube" type="playlist" id="..." filter="popular"]`

---

## 💻 Built With

- WordPress Plugin API  
- YouTube Data API  
- Twitch API  
- WP Cron & Transients  
- AJAX & Shortcodes

---

## 📌 License

MIT License or GPLv2 (to be decided based on distribution plan)

---

## 🙋‍♀️ Maintained by

[Making The Impact LLC](https://makingtheimpact.com)

---

> Created with ❤️ to help content creators connect with their audiences more efficiently.
