# WordCraft — adaLOCAL

Resep pemasangan **WordCraft** untuk [adaLOCAL](https://adacode.ai) di adaCODE App: dipasang di komputer pengguna dengan
satu klik, lalu agen AI adaCODE (adaVIBE & adaGENTIC) bisa memakainya lewat MCP tanpa setelan apa pun.

Pengolah kata ala Microsoft Word — ditulis dari nol dengan Rust. Buka & simpan DOCX, ekspor PDF, ringan dan offline, bisa disetir agen AI lewat MCP.

- App asli: https://github.com/storytold/wordcraft
- Lisensi app asli: MIT OR Apache-2.0 (repo ini hanya berisi resep pemasangan, bukan kode app-nya)

## Isi repo

| Berkas | Fungsi |
|---|---|
| `adacode.json` | Manifes: langkah `pasang` (zip portabel resmi v0.10.0 + cek SHA-256), cara `jalan`, `perbarui`, server `mcp`. Data JSON, bukan skrip. |
| `wordcraft.png`, `gambar.jpg` | Ikon (MIT/Apache-2.0, dari repo WordCraft) dan tangkapan layar resmi untuk kartu katalog. |

## MCP

`wordcraft-cli.exe mcp --automation-read-root <folder kerja> --automation-write-root <folder kerja>` — agen hanya bisa
membaca & menulis di folder kerja (folder proyek adaVIBE, atau `~/adaLOCAL` untuk adaGENTIC); jalur lain ditolak.

## Cara app ini masuk ke katalog adaLOCAL

Admin adaCODE mendaftarkan repo ini di `/admin/app-katalog` beserta **commit SHA lengkap**. Server mengambil
`adacode.json` pada commit itu, memeriksanya, lalu menyalinnya. Perubahan di repo ini **tidak** sampai ke pengguna
sampai admin meninjau dan menyimpan SHA baru. Jangan menulis rahasia di repo ini.
