# Pertemuan 11 - Dictionary/Map  
Nama: RIKI AGIL SAPUTRA


NIM: 2225250026


Kelas: 3A  
## Tujuan 
Memodelkan data pendidikan menggunakan dictionary dan pasangan key-value.  
## Struktur Data 
Jelaskan key utama dan value yang digunakan.  
key utama yang dipakai ada A001, A002, A003, A004, A005, A006. Masing masing key utama memiliki key lagi di dalamnya, yaitu nama, kelas, dan nilai. Setiap key nama, kelas, dan nilai memiliki value berupa nama, kelas, dan nilai bersesuaian dengan nim mahasiswa yang dimaksud.
Struktur Data `data_mahasiswa` (Nested Dictionary)
==================================================

data_mahasiswa = {
│
├── "A001" : { "nama": "Ayu",   "kelas": "A", "nilai": 85 },
├── "A002" : { "nama": "Budi",  "kelas": "A", "nilai": 82 },
├── "A003" : { "nama": "Citra", "kelas": "B", "nilai": 92 },
├── "A004" : { "nama": "Deni",  "kelas": "B", "nilai": 74 },
├── "A005" : { "nama": "Eka",   "kelas": "A", "nilai": 88 },
└── "A006" : { "nama": "Fajar", "kelas": "B", "nilai": 80 }
      │            │       │        │     │       │    │
      │            │       │        │     │       │    └─ Inner Value (Integer)
      │            │       │        │     │       └────── Inner Key (Atribut Nilai)
      │            │       │        │     └────────────── Inner Value (String)
      │            │       │        └──────────────────── Inner Key (Atribut Kelas)
      │            │       └───────────────────────────── Inner Value (String)
      │            └───────────────────────────────────── Inner Key (Atribut Nama)
      │
      └─► KEY UTAMA (Outer Key / NIM Mahasiswa)

## Cara Menjalankan 
python3 praktik/data_mahasiswa.py  
## Test Case 
 
| Kasus | Input/aksi | Hasil yang diharapkan | Hasil aktual | Status |
| :--- | :--- | :--- | :--- | :--- |
| Pencarian tersedia | A003 | Data Citra ditampilkan | Data Citra ditampilkan | Sesuai |
| Pencarian tidak tersedia | A999 | Pesan 'Data tidak ditemukan' | Pesan 'Data tidak ditemukan' | Sesuai |
| Pembaruan nilai | A002 menjadi 82 | Nilai A002 berubah menjadi 82 | Nilai A002 berubah menjadi 82 | Sesuai |
| Penambahan data | A006 | Key A006 tersedia setelah ditambahkan | Key A006 tersedia setelah ditambahkan | Sesuai |
| Rekap | items() | Semua NIM dan data tampil | Semua NIM dan data tampil | Sesuai |

## Refleksi 
Satu kesalahan akses key yang saya temukan adalah menampilkan nilai di dalam key utama dengan tanpa membuat pasangan terurut. Misalkan seharusnya saya menuliskan demikian:
print (mahasiswa["A001"]["nama"]) tetapi saya malah menuliskan secara demikian print (mahasiswa["A001"]["nama", "kelas"]). Lalu saya bisa atasi dengan membuatnya menjadi dua pasangan terurut menjadi print (mahasiswa["A001"]["nama"], mahasiswa["A001]["kelas"])