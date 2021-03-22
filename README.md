# yapt

Yet another pic torrent.

## Idea

- the given picture + payload + salt
- encoding the payload with salt, then split into 3 or 4 (or any) pieces
- upload each piece to different paste-bin
- convertor the paste-bin URL into QR code
- apply FFT on each channel of the picture, RGB/ARGB/CMYK (`len(channel) == len(pieces)`)
- set the last bit with the above QR code.
- IFFT the masked pic
- Done!
