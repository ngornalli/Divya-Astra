# ⚔️ Divya Astra: Celestial Warfare

**Divya Astra** is an immersive, multiplayer strategy card game based on legendary weapons (Astras) from Hindu mythology. Built with modern web technologies, it features real-time gameplay, a responsive "glassmorphism" UI, and dynamic data visualization.

![Game Banner](https://via.placeholder.com/1200x400/020617/f59e0b?text=DIVYA+ASTRA+-+Celestial+Warfare)
*(Replace this link with a screenshot of your actual game)*

---

## 🌟 Features

* **Real-Time Multiplayer:** powered by **Supabase** for instant state synchronization between players.
* **Mythological Lore:** Detailed cards featuring weapons like *Brahmastra*, *Sudarshana Chakra*, and *Trishula*.
* **Responsive Design:** optimized for Mobile (Vertical scrolling hand), Tablet, and Desktop (Dashboard view).
* **Visual Analytics:** Interactive **Radar Charts** and **Progress Bars** to visualize weapon stats.
* **Weapon Catalog:** A standalone "Museum" page to explore the history, lore, and stats of every weapon.
* **Host Controls:** Room creation, dynamic hand-size selection (3-30 cards), and game flow management.

---

## 🎮 Game Rules

The game functions similarly to "Trump Cards" or "War".

1.  **The Deck:** The game contains a set of legendary weapons, each with 6 attributes:
    * 🔥 **Destruction:** Raw damage potential.
    * 🎯 **Precision:** Accuracy of the strike.
    * 📡 **Range:** Effective distance.
    * ⚡ **Speed:** Velocity of attack.
    * 🛡️ **Durability:** Weapon resilience.
    * ✨ **Mysticism:** Spiritual/Magical energy.

2.  **The Objective:** Win rounds by selecting the strongest attribute of your current weapon to defeat your opponents' weapons.

3.  **The Flow:**
    * **Start:** Each player is dealt a hand of cards (determined by the Host).
    * **Turn:** The "Active Player" (Commander) selects a card from their hand and chooses **ONE attribute** (e.g., Speed) to attack with.
    * **Response:** All other players must select a card from their hand to defend against that specific attribute.
    * **Clash:** Once all players have selected, the cards are revealed.
    * **Resolution:** The card with the **highest value** in the chosen attribute wins the round. The winner gains points.
    * **Next Round:** The cards are discarded, and the turn passes to the next player.

4.  **Victory:** The player with the highest score when all cards are played wins the war.

---

## 🕹️ How to Play

### 👑 For the Host (Commander)
1.  Open the game and click **CREATE SQUAD**.
2.  Enter your Codename.
3.  You will be taken to the Lobby. **Share the Sector ID (Room Code)** with your friends.
4.  Wait for players to appear in the lobby list.
5.  Select the **Number of Cards** per player (3 to 30) using the dropdown.
6.  Click **INITIATE WAR** to start the game.
7.  *Note:* Only the Host can advance rounds or force-skip lagging players.

### 🛡️ For Players (Operatives)
1.  Open the game and click **JOIN SQUAD**.
2.  Enter your Codename and the **4-Character Sector ID** provided by the Host.
3.  Wait in the lobby until the Host starts the game.
4.  When the game starts:
    * **If it's your turn:** Select a card, then click an attribute (e.g., Destruction) to attack.
    * **If it's not your turn:** Wait for the attacker to choose an attribute, then select your best card to defend against it.

---

## 🛠️ Technology Stack

* **Frontend:** HTML5, CSS3 (Tailwind CSS via CDN), Vanilla JavaScript.
* **Backend / Realtime:** Supabase (PostgreSQL + Realtime Subscriptions).
* **Icons:** Lucide Icons.
* **Effects:** Canvas Confetti.
* **Fonts:** Google Fonts (Cinzel, Inter, JetBrains Mono).

---

## 📂 Project Structure

```text
/divya-astra
│
├── index.html        # Main Game Logic & UI (Lobby, Game, Results)
├── catalog.html      # Weapon Catalog / Encyclopedia Page
├── README.md         # Documentation
└── image/            # Folder containing weapon images
    ├── 1.jpg
    ├── 2.jpg
    └── ...           (Images must match IDs in database: 1.jpg, 2.jpg)
