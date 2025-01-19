# STB-Portal-Json-To-M3u-Convert
# JSON to M3U Converter

This Python script converts a JSON IPTV channel file into an M3U playlist and extracts EPG (Electronic Program Guide) sources into a separate text file.

## Features

- Converts JSON IPTV channel data to M3U format.
- Extracts EPG URLs and saves them to a file (`epg_sources.txt`).
- Handles channel details like name, logo, and group title.
- Skips channels without valid stream URLs.

## Requirements

- Python 3.6 or higher.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/json-to-m3u.git
   cd json-to-m3u


Install dependencies (if needed):
bash
Copy
Edit
pip install -r requirements.txt
Usage
Place your channels.json file in the same directory as the script.

Run the script:

bash
python json_to_m3u.py
The script generates:

tata_playlist_with_epg.m3u: The M3U playlist.
epg_sources.txt: A file containing unique EPG URLs.
Input JSON Format
The JSON file should follow this structure:

json
{
    "js": {
        "data": [
            {
                "id": "12345",
                "name": "Channel Name",
                "xmltv_id": "channel.id",
                "genre_str": "Category",
                "logo": "http://example.com/logo.png",
                "cmds": [
                    {"url": "http://example.com/stream.m3u8"}
                ],
                "epg": [
                    {"url": "http://example.com/epg.xml"}
                ]
            }
        ]
    }
}
Example Output
M3U Playlist (tata_playlist_with_epg.m3u)
m3u
#EXTM3U
#EXTINF:-1 tvg-id="channel.id" tvg-name="Channel Name" group-title="Category" tvg-logo="http://example.com/logo.png",Channel Name
http://example.com/stream.m3u8
EPG Sources (epg_sources.txt)
arduino
Copy
Edit
http://example.com/epg.xml
Contributing
Fork the repository.
Create a new branch (git checkout -b feature/your-feature-name).
Commit your changes (git commit -m 'Add your message').
Push to the branch (git push origin feature/your-feature-name).
Open a Pull Request.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Author
Developed by [Kobir Shah](https://github.com/MohammadKobirShah).
