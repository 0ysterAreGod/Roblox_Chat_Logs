# Roblox_Chat_Logs
Usernamex User Interaction Dataset (RUID-2025)

**Status:** Active | **Data Type:** Chat Logs / Metadata | **Focus:** Social Dynamics & Trust and Safety

### 📄 Abstract
This repository serves as a digital archive documenting user interactions, linguistic patterns, and behavioral trends within unmoderated "social hangout" environments on the Roblox platform. 

The primary goal of this project is to provide a raw dataset for analyzing:
*   **Toxicity trends** in VoIP-enabled and text-based gaming servers.
*   **Scam bot automation patterns** (e.g., cookie logging phish attempts).
*   **"E-Gangster" subcultures:** The linguistic markers and hierarchy dynamics of exploit-adjacent communities.
*   **Moderation gaps:** Identifying keywords and behaviors that bypass current standard filtration systems.

### 📂 Methodology
Data is collected via automated client-side logging agents running on Android instances. These agents utilize `TextChatService` listeners to capture:
1.  **Chat Content:** Raw text strings as displayed to the client.
2.  **Proximity Data:** The physical distance (in studs) between speakers to distinguish between public broadcasting and private conversation.
3.  **Account Metadata:** Account age and persistent UserIDs to differentiate between "burner" accounts and legitimate long-term users.

### 📝 Data Format
Each file represents a single server session. The naming convention is `Log_YYYY-MM-DD_HH-MM-SS.txt`.

**File Header:**
```text
==================================================
GAME: [Game Name] [Place ID]
SERVER JOB ID: [UUID]
DATE: MM/DD/YY | TIME: HH:MM:SS
TOTAL PLAYERS: [Count]
==================================================
```

**Entry Format:**
```text
[Timestamp] [Distance] [Account Age] [UserID] DisplayName (@Username): Message
```

**Example Entry:**
```text
[06:45:00] [Dist:205] [Days:112] [ID:9113073738] KizmoBoys (@Wassasubi12): Join /robloxbans today
```
*(Note: The above example demonstrates a common scam bot pattern captured within the dataset.)*

### ⚠️ Ethics & Disclaimer
**This repository is strictly for educational, archival, and research purposes.**

1.  **No Harassment:** The inclusion of UserIDs is necessary for longitudinal data analysis (tracking recidivism and account flipping). It is **not** an invitation to harass, mass-report, or contact any individuals listed in these logs.
2.  **Raw Data:** These logs contain unfiltered language, including slurs, hate speech, and sexually explicit text. Viewer discretion is advised.
3.  **Privacy:** This project does not log IP addresses or real-world Personal Identifiable Information (PII) beyond what users voluntarily broadcast in a public chat server.

### 🧠 Potential Use Cases
*   **Natural Language Processing (NLP):** Training models to detect toxicity, sarcasm, or grooming behavior.
*   **Scam Prevention:** Analyzing the syntax of "free Robux" or "ban appeal" scam bots to create better regex filters.
*   **Sociological Study:** Analyzing the correlation between "Account Age" and toxic behavior.

---
*Maintained by [0yster]Analyzinglection is ongoing.*
