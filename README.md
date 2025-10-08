# 🏋️‍♂️ Gym Class Auto-Booking Bot
- A Python + Selenium automation script that logs in to your gym portal and automatically books all Tuesday and Thursday 6:00 PM classes.
- Built for reliability — includes retries, wait conditions, and verification of successful bookings.

---

# 🚀 Features
- ✅ Automatic login using saved credentials
- 🔁 Retries actions when elements are slow to load
- 📅 Filters and books only Tuesday/Thursday 6 PM classes
- 🕒 Detects already booked or waitlisted classes
- 🔍 Verifies bookings under the “My Bookings” section
- 🧠 Human-readable console output and status tracking

---
# 🧩 Tech Stack
- Language: Python 3.8+
- Libraries:
  - selenium
  - time, os, re (standard libraries)

---

# ⚙️ Installation

1. Clone the repository
```bash
git clone https://github.com/YOUR-USERNAME/gym-booking-bot.git
cd gym-booking-bot
```
2. Install dependencies
```bash
pip install -r requirements.txt

```
3. (Optional) Ensure you have Chrome installed and the ChromeDriver version matches your Chrome version.
You can check your version at:
https://chromedriver.chromium.org/downloads

 ---

 # 🔑 Configuration
 Open gym_booking.py and update your credentials:
 ```python
ACCOUNT_EMAIL = "your_email@example.com"
ACCOUNT_PASSWORD = "your_password"
GYM_URL = "https://appbrewery.github.io/gym/"

```

----

# ▶️ Usage
Run the script:
```bash
python gym_booking.py

```
It will:
1. Launch Chrome using a persistent profile folder (chrome_profile/)
2. Log in to the gym site
3. Book all Tuesday/Thursday 6:00 PM classes
4. Verify the bookings on your “My Bookings” page
5. Print a summary like this:
```pgsql
✓ Successfully booked: Yoga Class on Tuesday
✓ Verified: Yoga Class
✅ SUCCESS: All bookings verified!

```
----
# 📁 Folder Structure
```bash
gym-booking-bot/
│
├── gym_booking.py         # Main automation script
├── requirements.txt       # Python dependencies
├── .gitignore             # Ignore cache and Chrome profile
└── README.md              # Documentation

```
---
# ⚠️ Notes & Troubleshooting
- If Chrome closes immediately, make sure detach=True is set in ChromeOptions.
- If login fails, verify your credentials and gym portal URL.
- For “element not found” errors, check if the page structure or IDs changed on the website.
- You can clear your Chrome profile by deleting the chrome_profile/ folder.
---
# 🧠 Future Enhancements
- Add environment variable support for credentials
- Add email or WhatsApp notifications for booking success
- Convert script into a Flask-based web app for one-click booking
---
# 👨‍💻 Author
- Sayan Sanki
- 📧 [sayansanki1997@gmail.com]
- 💼 Passionate about automation, Python, and AI projects.

