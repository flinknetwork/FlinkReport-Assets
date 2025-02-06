# Flink – Organization-Based Social Network

## Overview

**Flink** is a private social networking platform designed exclusively for universities, workplaces, and other organizations. Access is restricted to users with official organization-provided email IDs, ensuring authenticity and a controlled user base. The app serves as an internal communication and networking platform, integrating features like a directory, chat system, college/company news, engagement rankings, polls, quizzes, and a swipe-based profile discovery system.

## Core Features

### 1. **Verified Organization-Only Access**
- Users must sign up with an official email ID from their organization (e.g., @saveetha.com).
- Ensures only verified students/employees gain access, preventing spam.
- Explicit permission from organizations is not currently obtained.

### 2. **User Profiles & Directory**
- Users can create profiles with name, department, college, bio, images, and other details.
- Searchable directory for students/employees categorized by name, department, or role.
- **Profile Swiping** (Tinder-like UI): Users can swipe through profiles, but only "like" is allowed (no rejection option). Liked profiles can be revisited.

### 3. **College/Company News & Events**
- Organizations can post announcements, events, and updates.
- Acts as an internal communication hub for verified members.
- Includes a section for public love letters, manually selected and uploaded.

### 4. **Controlled Chat System**
- Users can request to connect and chat. Chats are enabled only after mutual approval.
- Bad word filter implemented using an array of restricted words.
- **Important Notes**:
  - No end-to-end encryption for messages stored in the database.
  - No active moderation of chats; users can report or block inappropriate messages.
  - **POSH Act Considerations**:
    - No prevention for harassment or inappropriate messages before they are sent.
    - Users must report offensive content manually.
    - No AI-based moderation or filtering beyond basic word restriction.

### 5. **Engagement & Streak System**
- Like-based ranking system: Users gain visibility based on engagement.
- **Snapchat-style Streaks**: Users can maintain streaks for continuous interaction.

### 6. **Polls, Quizzes & Interactive Content**
- Polls and quizzes are manually fed into the app.
- Users can participate and engage with interactive content.

### 7. **Third-Party API Integrations**
- **RoxyAPI Astrology Horoscope** – Provides zodiac sign predictions.
- **DOTA API** – Fetches daily sports news.
- **Meme-API** – Provides trending memes.
- **api.api-ninjas.com/v1/quotes** – Fetches daily quotes (content not controlled by Flink).

### 8. **Automated Form & Weekly Reports**
- Integrated Google Form automation for students/employees to submit weekly reports.
- Users are notified automatically to fill out reports.

## User Data Collection & Permissions

### **Data Collected from Users**

| Field          | Type   | Editable | Notes                               |
|----------------|--------|----------|-------------------------------------|
| Name           | String | ✅ Yes   |                                     |
| Register Number| String | ❌ No    | One-time entry                     |
| Phone Number   | String | ✅ Yes   |                                     |
| DOB            | Date   | ❌ No    | One-time entry                     |
| Department     | String | ❌ No    | One-time entry                     |
| Gender         | String | ✅ Yes   |                                     |
| Blood Group    | String | ✅ Yes   |                                     |
| Languages      | Array  | ✅ Yes   | Default: []                        |
| Hobbies        | Array  | ✅ Yes   | Default: ["Nothing"]               |
| Native Place   | String | ✅ Yes   |                                     |
| College        | String | ❌ No    | One-time entry                     |
| College Year   | String | ✅ Yes   |                                     |
| Bio            | String | ✅ Yes   |                                     |
| Password       | String | ✅ Yes   | Hashed                              |
| FCM Token      | String | ✅ Yes   | Used for push notifications         |
| Profile Images | Array  | ✅ Yes   | Default: Placeholder image          |

### **Permissions Used**
- **GPS** – Location tracking (if needed in future updates).
- **Storage** – Profile images and other media.
- **Notifications** – Push notifications for updates, messages, and reminders.

## Security & Privacy Risks
- Email verification is reliable, but organizations have not given explicit approval.
- No end-to-end encryption in messages, making chat data readable in the database.
- Bad word filter is basic, and cannot prevent all forms of inappropriate messages.
- Users must manually report/block bad actors; no AI moderation for offensive content.
- External APIs are used for astrology, sports news, memes, and quotes, meaning Flink has no control over the API content.

## Monetization & Future Plans
- **Planned paid features**:
  - See who viewed your profile.
  - Increased messaging quota.
  - Ability to post public letters/news.
  - Possible introduction of ads in the future.

## App Store & Play Store Deployment

### **Uploading to Play Store**
- Google Play requires a Google Developer Account ($25 one-time fee).
- App submission requires:
  - App APK/AAB file.
  - Privacy Policy (required for handling user data).
  - Screenshots & Description.
  - App Category & Rating (set based on content).

### **Pricing Models**
- Can be released as free or with in-app purchases (IAPs).
- Flink may later charge for premium features like profile insights, boosted messages, and announcements.

## Maintenance & Updates

### **Regular Updates**
- Feature additions, UI improvements, bug fixes.

### **Bug Fixing & Patch Releases**
- Minor updates to fix reported issues.

### **Security Updates**
- Address vulnerabilities or exploits.

### **Force Update vs. Auto-Update**
- **Auto-Update**: Users receive updates automatically when they update apps through the Play Store.
- **Force Update**: A mandatory update can be implemented via version checks on app launch. Users will be forced to update before accessing the app.

---

## Final Notes

Flink is a promising organization-based social network with unique engagement features and a verified user base. However, security concerns such as unencrypted messages, lack of active moderation, and external API reliance need attention. Monetization through premium features and ads can sustain future growth, and legal considerations (such as explicit email approval from organizations) should be addressed.

---

**Contributions, Issues, and Feedback** are welcome! Feel free to fork the repository, open an issue, or send a pull request.

---
