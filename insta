import os
import random
from instagrapi import Client

# List of Yuvan Shankar Raja songs/lyrics to cycle through
YUVAN_SONGS = [
    "🎵 High on Love - Pyaar Prema Kadhal",
    "🎵 Kadhal Aasai - Anjaan",
    "🎵 Pogadhe - Deepavali",
    "🎵 Oru Kal Oru Kannal - Siva Manasula Sakthi",
    "🎵 Venmegam - Yaaradi Nee Mohini",
    "🎵 En Kadhal Solla - Paiyaa",
    "🎵 Idhu Varai - Goa",
    "🎵 Kaatrukku Veliyidai - Song Vibe",
    "🎵 Aathadi Aathadi - Anegan",
    "🎵 Loosu Penne - Vallavan"
]

def update_instagram_note():
    username = os.environ.get("IG_USERNAME")
    password = os.environ.get("IG_PASSWORD")

    if not username or not password:
        raise ValueError("Instagram credentials are not set in environment variables.")

    # Select a random Yuvan song
    today_song = random.choice(YUVAN_SONGS)

    cl = Client()
    # Log in to Instagram
    cl.login(username, password)

    # Post/Update the Instagram Note
    # Note: Text limit for Instagram Notes is 60 characters
    cl.create_note(text=today_song, audience=0)  # audience=0 is for 'Followers you follow back' or 'Close Friends' depending on API defaults
    print(f"Successfully updated note to: {today_song}")

if __name__ == "__main__":
    update_instagram_note()
