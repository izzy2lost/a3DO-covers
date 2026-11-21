# a3DO cover pack

Full-wrap box art (back, spine, front) for the a3DO emulator's cover carousel.
The app's **Settings → Box art → Download covers** reads `covers/covers.txt`
and fetches only the images it does not already have.

- `covers/<game>.jpg` is the US (NTSC-U) cover, named after the game's
  [Redump](http://redump.org/) title, so discs named the Redump way
  ("Family Feud (USA).chd" -> `familyfeud.jpg`) match exactly. `_eu` is the PAL cover and `_jp`
  the Japanese one. Each game in the library gets its own region's cover when
  there is one, and the US cover otherwise.
- Images are 640 px tall, scaled from scans gathered from
  thecoverproject.net and arcadeartwork.org. The artwork belongs to its
  publishers.

To add or replace covers, rebuild the folder with `tools/covers/make_cover_pack.py`
from the emulator's repository and commit the result:

    python3 tools/covers/make_cover_pack.py ~/Desktop/3DO_Covers covers \
        --dat tools/covers/redump-3do.dat

It prints every scan it matched to a Redump title by anything other than its
exact name; fix a wrong match with a line in `tools/covers/aliases.txt`.
