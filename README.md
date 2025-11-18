zmk-config for charybdis (4x6)

ada update baru remap tanpa flash
https://zmk.studio/

ZMK Codes Docs https://zmk.dev/docs/codes


Untuk cara fork repository ini :

ZMK Keymap Editor https://nickcoutsos.github.io/keymap-editor/ Tutorial Mapping ZMK https://youtu.be/cAi5pnkz48M

Setelah firmware di download, tekan 2x tombol reset saat USB terhubung. lalu tinggal extract dan drop file .uf2 nya di disk bootloader.




Charybdis 4x6 Versi Bluetooth Dual-Mode — Shortcut Default & Penjelasan Pengikatan/Penggantian Kanal Bluetooth

1. Lokasi Tombol Flashing Firmware
Setelah memasang kabel data, tekan dua kali tombol flashing dengan cepat (kurang dari 0,5 detik). Komputer akan muncul sebagai drive USB dan firmware dapat diseret ke dalam drive tersebut untuk flashing. Hanya pengguna berpengalaman yang disarankan melakukan ini.

<img width="1754" height="1103" alt="Image" src="https://github.com/user-attachments/assets/07a923d0-8b90-47b0-af16-2b3c3918968e" />
 
Related keyboard shortcuts: Three layers are enabled by default; you can add more yourself. Source code is open source: Open source address:

https://github.com/emjetech/zmk-for-charybdis/tree/Charybdis_4x6_Studio

Tekan S untuk Snipe mode dan F untuk Scrolling.

Shortcut sesuai gambar pada dokumen:
1.	MO(1) + baris pertama = F1 ~ F12
2.	MO(1) + DELETE (atau MO(1) + H) = klik kiri mouse
3.	MO(1) + Space (atau MO(1) + J) = klik kanan mouse
4.	Tombol F ditekan dan ditahan = masuk mode scroll
Trackball dapat menggulir tampilan. Lepaskan untuk kembali ke mode pointer.
5.	Tombol S ditekan dan ditahan = masuk sniper mode
DPI trackball turun menjadi 400 DPI untuk kontrol sangat presisi. Lepaskan untuk kembali ke DPI default (1200 DPI).
6.	MO(2) + A = hapus semua ikatan kanal Bluetooth
7.	MO(2) + C = hapus ikatan kanal Bluetooth yang sedang aktif
8.	MO(2) + N = pindah ke kanal Bluetooth berikutnya
9.	MO(2) + 1–5 = pindah ke kanal Bluetooth 1–5
________________________________________
Tips Menggunakan Kanal Bluetooth
Misalnya Anda memiliki 5 perangkat Bluetooth:
1.	HP Android
2.	iPhone
3.	Laptop
4.	PC Desktop
5.	Laptop milik teman

Cara menggunakannya:
•	Tekan MO(2) + 1 → pilih kanal 1 → lakukan pairing → jika berhasil, kanal 1 telah terhubung dengan perangkat 1
•	Ulangi untuk kanal 2–5 menggunakan MO(2) + 2 … MO(2) + 5
Dengan cara ini, Anda dapat berpindah antar 5 perangkat dengan mudah hanya menggunakan shortcut MO(2) + nomor.
Jika ingin mengganti perangkat pada suatu kanal (misal kanal 1):
1.	Tekan MO(2) + 1 untuk masuk ke kanal 1
2.	Tekan MO(2) + C untuk menghapus ikatan kanal tersebut
3.	Pairing ulang dengan perangkat baru

MO(2) + A menghapus semua ikatan Bluetooth sekaligus — jarang diperlukan.
Jika suatu hari keyboard tidak terhubung ke perangkat:
•	selain kemungkinan baterai habis,
•	bisa jadi Anda tidak sengaja menghapus ikatan kanal Bluetooth,
Coba ulangi pairing pada kanal tersebut.
⚠️ Catatan:
Versi ZMK Bluetooth bersifat open-source dan memiliki beberapa bug kecil, misalnya:
•	flashing gagal pada percobaan pertama,
•	Bluetooth bisa terhubung ke HP tapi tidak ke PC,
dll.
Biasanya ini terjadi karena firmware tidak ter-flash dengan benar.
Pengguna pemula disarankan tidak melakukan modifikasi berlebihan. Tidak ada garansi gratis jika firmware rusak akibat flashing.
________________________________________





3. Panduan Singkat Flashing Firmware
Secara umum, keyboard bawaan pabrik sudah memiliki firmware dan bisa langsung digunakan setelah memasang keycaps dan switch.
Namun, jika Anda mengubah keymap atau fitur tertentu, Anda perlu mem-flash firmware baru.
Kesalahan yang sering terjadi:
•	pengguna langsung mem-flash firmware kiri & kanan tanpa reset
→ menyebabkan keyboard tidak bisa digunakan, tidak terhubung Bluetooth, sisi kiri tidak berfungsi, atau bahkan keduanya mati.
Dalam satu paket hasil build firmware biasanya terdapat 3 file:
1.	Firmware tangan kiri
2.	Firmware tangan kanan
3.	Firmware reset
Urutan flashing yang benar:
1.	Flash firmware reset ke kedua sisi (kiri & kanan)
2.	Flash firmware kiri ke sisi kiri
3.	Flash firmware kanan ke sisi kanan
Jika masih tidak berfungsi, ulangi proses beberapa kali.


________________________________________
4. Catatan Sangat Penting Saat Memasang/Mengganti Switch

Keyboard ini mendukung hot-swap, tetapi karena casing memiliki permukaan melengkung, posisi setiap lubang switch tidak berada pada satu bidang datar.
Akibatnya:
•	switch sangat mudah masuk miring,
•	jika ditekan terlalu kuat, socket bisa terlepas,
•	bahkan dapat merusak PCB (meskipun bisa diperbaiki dengan fly-wire, tapi 
merepotkan).
Cara pemasangan switch yang aman:
1.	Setelah keyboard diterima, lepas bottom case, dan kalau bisa lepas mainboard juga.
2.	Saat memasang switch:
o	satu jari menekan switch dari depan,
o	satu jari lagi menahan socket hot-swap di belakang PCB,
o	tekan kedua sisi secara bersamaan. 
 <img width="926" height="1235" alt="Image" src="https://github.com/user-attachments/assets/a47c42f3-90d3-4279-8eed-0261e3bf3f2c" />
 <img width="926" height="1235" alt="Image" src="https://github.com/user-attachments/assets/7fee569d-68c1-400d-8ab6-c7623f03b4e2" />

Keuntungan metode ini:
•	sekuat apa pun tekanan Anda, socket tidak akan rusak,
•	jika terasa keras, berarti switch tidak sejajar — cabut dan pasang kembali dengan benar.
Metode ini terbukti aman dan hampir tidak mungkin merusak socket.

