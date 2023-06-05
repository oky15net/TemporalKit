# TemporalKit

Sebuah solusi all-in-one untuk menambahkan Stabilitas Temporal ke Render Difusi Stabil melalui ekstensi otomatis1111.

*Anda harus menginstal FFMPEG ke dalam path sebelum menjalankannya.*

Anda dapat melihat demonstrasi dengan satu batch di sini:

https://twitter.com/CiaraRowles1/status/1645923461343363072

Dan demonstrasi batch di sini:

https://mobile.twitter.com/CiaraRowles1/status/1646458056803250178

Tutorial Ebsynth:

https://twitter.com/CiaraRowles1/status/1648462374125576192

CATATAN: EBSYNTH TIDAK MENDAFTARKAN KEYFRAME JIKA ANDA MENGGUNAKAN DI ATAS 20,

Tutorial pemisahan bingkai Ebsynth:

https://www.youtube.com/watch?v=z3YNHiuvxyg&ab_channel=CiaraRowles

Contoh hasil yang dapat Anda peroleh:

https://user-images.githubusercontent.com/13116982/234425054-9a1bbf30-93a8-4f5b-9e80-4376ab3c510a.mp4

Nilai-nilai dalam ekstensi ini adalah sebagai berikut:

FPS: Ini adalah fps video yang diekstrak dan diproduksi.

batch_Size: ini adalah jumlah bingkai antara setiap keyframe, jadi misalnya jika Anda memiliki fps 30, dan ukuran batch 10, maka akan membuat 3 keyframe per detik dan memperkirakan sisanya.

per side: ini adalah akar kuadrat dari jumlah bingkai per piring, jadi misalnya nilai per side 2 akan membuat 4 piring, 3 akan membuat 9 piring, 4 akan membuat 16 piring.

Resolusi: ukuran setiap piring, disarankan untuk mengatur ini menjadi kelipatan variabel per side Anda.

pengaturan batch: buka drop down ini hanya jika Anda ingin menghasilkan folder piring.

Max Frames: saat menghasilkan folder piring, ini mengatur berapa banyak bingkai pada fps di atas yang ingin Anda dapatkan, kemudian membaginya menjadi piring dalam kelompok (per side * per side * batch size)

Border Frames: setiap piring yang dihasilkan dalam batch akan berisi sejumlah bingkai dari piring berikutnya dan mencampur di antara mereka.

Folder Batch: Jika Anda menghasilkan batch piring, tentukan folder kosong dan saat mengklik run, itu akan mengisinya dengan folder dan file terkait, yang perlu Anda lakukan hanyalah pergi ke pemrosesan batch img2img di sd asli, masukkan folder input yang baru dibuat sebagai input, folder output yang baru dibuat sebagai output, hasilkan, kembali ke Tab Batch-Warp temporal-kit, masukkan seluruh direktori folder dan klik baca dan itu akan mengatur semuanya.

Resolusi Output (di tab warp batch): resolusi maksimum di salah satu sisi video output.

FAQ:

Q: video saya menghasilkan smearing.

A: gunakan fps yang lebih tinggi dan/atau nomor batch yang lebih rendah, semakin dekat keyframes, semakin sedikit artefak.

#TODO
- Mengatur penskalaan berbasis difusi untuk output piring
- Mengaktifkan tombol img2

img untuk pemrosesan batch.
- Menambahkan pengecekan untuk melihat apakah folder output sudah ditambahkan.
- Memperbaiki kesalahan shutdown aneh setelah dijalankan.
- Menghubungkan ke API.
- Mendukung ekspor/impor flowmaps dari mesin permainan.

Terima kasih kepada RAFT untuk sistem aliran optik.
