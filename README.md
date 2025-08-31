# Nối Từ Discord Bot

A feature-rich Vietnamese word-chain (Nối Từ) Discord bot built with **discord.py**.  
It supports casual play, tournaments, ranking systems, anti-cheat, and database persistence.

---

## ✨ Features

- 🎮 **Game Modes**
  - Normal mode: play casually or competitively with friends.
  - Tournament mode: team-based competition with ranking and streak bonuses.
  - Practice mode: play against the bot with multiple difficulty levels (easy → insane).

- 🧠 **AI Opponent**
  - Built-in strategic bot using search algorithms (Negamax, IDDFS, heuristics).
  - Supports difficulty levels: `easy`, `medium`, `hard`, `insane-min`, `insane-mid`, `insane-max`.

- 🏆 **Ranking System**
  - Individual rank points and streak tracking.
  - Team leaderboard (**Hall of Fame**) with streaks and seasonal resets.
  - Automatic bonus points for winning streaks.

- 🔒 **Anti-Cheat**
  - Auto-play detection (too fast inputs).
  - Rare/invalid word checks using frequency analysis and online dictionary validation.
  - Warnings, auto-bans, and rank penalties for violators.

- 💾 **Database Integration**
  - Persistent storage via SQLite (`databases.db`).
  - Stores dictionary phrases, user stats, teams, and season info.

- ⚙️ **Admin Tools**
  - Manage dictionary (`add_word`, `remove_word`, `reload_dict`).
  - Control user stats (`set_rank`, `set_streak`, `ban`, `warn`, etc.).
  - Manage tournaments and teams (`create_team`, `start_match`, `add_member`, etc.).

---

## 🚀 Installation

### 1. Clone the repository
```bash
git clone https://github.com/EndermanPC/Noi-Tu.git
cd Noi-Tu
````

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure your bot

* Open `main.py`.
* Replace the placeholder admin ID:

  ```python
  ADMIN = 999999999999999999  # ❌ placeholder
  ADMIN = YOUR_DISCORD_ID     # ✅ replace with your actual Discord ID
  ```
* Replace the placeholder bot token:

  ```python
  bot.run("YOUR_DISCORD_BOT_TOKEN") # ❌ placeholder
  bot.run("MTnx...Vg")              # ✅ replace with your actual Discord Bot Token
  ```

### 4. Run the bot

```bash
python main.py
```

---

## 📋 Requirements

* Python 3.9+
* Dependencies (from `requirements.txt`):

  * `discord.py`
  * `requests`
  * `wordfreq`

---

## 🔑 Commands

* `NTstart` → start a new game.
* `NTstop` → stop the current game (creator only).
* `NTsurrender` → surrender the current game.
* `NTrule` → show game rules.
* `NTrank` → show personal ranking.
* `NThalloffame` → show team leaderboard.
* `NTstart_bot <difficulty>` → play against the bot.

(See in-bot `NThelp` or `NTrule` for the full command list.)

---

## 📊 Data Persistence

* **SQLite** (`databases.db`) is used to store:

  * Phrases dictionary
  * User stats
  * Team data
  * Seasonal info

All data is auto-saved and loaded at runtime.

---

## 🛡️ Important Notes

* Ensure you **replace the `ADMIN` ID** in `main.py` with your actual Discord user ID.
* The bot must be invited to your Discord server with the following permissions:

  * `Send Messages`
  * `Read Message Content`
  * `Add Reactions`
  * `Manage Messages` (optional for tournaments/admin commands).

---

## 📦 Sample Database

If you want to try the bot with a **pre-built dictionary and database**,
please **contact me directly** and I will share the sample `databases.db` file.

---

## 🤝 Contact & Demo

* Try the bot here:
  [Invite Link](https://discord.com/oauth2/authorize?client_id=1396131015843385437&permissions=274877978688&integration_type=0&scope=bot)

* Contact me on Discord: **`twentyzr`**

---

## 📜 License

This project is released under the **Apache License 2.0**.
Feel free to modify and use it for your own Discord servers.
