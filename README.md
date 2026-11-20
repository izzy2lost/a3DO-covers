# a3DO cover pack

Full-wrap box art (back, spine, front) for the a3DO emulator's cover carousel.
The app's **Settings → Box art → Download covers** reads `covers/covers.txt`
and fetches only the images it does not already have.

- `covers/<game>.jpg` is the US (NTSC-U) cover, `_eu` the PAL one, and `_jp`
  the Japanese one. Each game in the library gets its own region's cover when
  there is one, and the US cover otherwise.
- Images are 640 px tall, scaled from scans gathered from
  thecoverproject.net and arcadeartwork.org. The artwork belongs to its
  publishers.

To add or replace covers, rebuild the folder with `tools/covers/make_cover_pack.py`
from the emulator's repository and commit the result:

    python3 tools/covers/make_cover_pack.py ~/Desktop/3DO_Covers covers
