# Telegram Voice Chat King

UserBot Telegram untuk Memutar Audio dalam Obrolan Suara.

Ini juga merupakan kode sumber dari userbot yang digunakan untuk bermain
DJ/Live Mengatur musik [VC DJ/Live Di](https://t.me/King-Userbot) grup Support.

Dianjurkan untuk digunakan [tgcalls](https://github.com/MarshalX/tgcalls)
Anda [Pyrogram Smart Plugin](https://docs.pyrogram.org/topics/smart-plugins)

Dianjurkan untuk digunakan [tgmusicuserbot](https://github.com/apisuserbot/tgvc-King)
bersama dengan userbot ini.

## Deploy ke Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/apisuserbot/tgvc-King/tree/dev)


Cek [smart-plugins](https://github.com/callsmusic/tgvc-userbot/tree/smart-plugins)
branch Jika Anda ingin menggunakan plugin `radio` atau` recorder`.
## Introduction

**Fitur**

- Playlist, queue
- Loop one track when there is only one track in the playlist
- Automatically downloads audio for the first two tracks in the playlist to
  ensure smooth playing
- Automatically pin the current playing track
- Show current playing position of the audio
- Daftar putar, antrian
- Ulangi satu trek jika hanya ada satu trek di daftar putar
- Secara otomatis mengunduh audio untuk dua trek pertama dalam daftar putar ke
  memastikan permainan yang lancar
- Secara otomatis menyematkan trek yang sedang diputar
- Tampilkan posisi pemutaran audio saat ini

**Cara Penggunaan**

Anda tidak dapat bermain dan mendengarkan dalam obrolan suara yang sama pada saat yang sama
disarankan untuk menjalankan userbot dengan akun alt Anda dan mengontrol userbot tersebut
dengan akun utama Anda dengan menambahkan akun utama Anda sebagai kontak alt
Akun. 

1. Jalankan userbot, coba perintah `! Ping`,`! Uptime` atau `! Sysinfo` untuk memeriksa apakah
   bot itu sedang berjalan.
2. kirim `! Join` ke obrolan grup yang mendukung obrolan suara dari akun userbot itu sendiri
   atau kontaknya, pastikan untuk menjadikan akun userbot sebagai admin grup dan berikan
   itu setidaknya izin berikut:
    - Hapus pesan
    - Kelola obrolan suara (opsional)
3. balas audio dengan `/ play` untuk mulai memutarnya di obrolan suara, setiap
   anggota grup dapat menggunakan perintah umum seperti `/ play`,` / current`
   dan `! help` sekarang.
4. periksa `! Help` untuk perintah lainnya

## Telegram Music
![Logo Project](https://telegra.ph/file/0defa48ac7a3c240cc5a0.jpg)

• Music dan tgvc adalah seputar bot dan userbot yang di gunakan untuk menghibur warga telegram dengan pesan bersuara!
   🐱 Channel Update : @MusicPr0jEctTElegram

## Run

Pilih salah satu dari dua metode dan jalankan userbot dengan
`python userbot.py`, hentikan dengan <kbd> CTRL + c </kbd>. Contoh berikut mengasumsikan
bahwa Anda akan menggunakan plugin `vc.player` dan` ping`, ganti
`api_id`,` api_hash` ke nilai Anda sendiri.

### Method 1: use config.ini

Create a `config.ini` file

```
[pyrogram]
api_id = 1234567
api_hash = 0123456789abcdef0123456789abcdef

[plugins]
root = plugins
include =
    vc.player
    ping
    sysinfo
```

### Method 2: write your own userbot.py

Replace the file content of `userbot.py`

```
from pyrogram import Client, idle

api_id = 1234567
api_hash = "0123456789abcdef0123456789abcdef"

plugins = dict(
    root="plugins",
    include=[
        "vc.player",
        "ping"
    ]
)

app = Client("tgvc", api_id, api_hash, plugins=plugins)
app.start()
print('>>> KING STARTED')
idle()
app.stop()
print('\n>>> KING STOPPED')
```

# License

AGPL-3.0-or-later

```
tgvc-userbot, Telegram Voice Chat Userbot
Copyright (C) 2021  Dash Eclipse

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
