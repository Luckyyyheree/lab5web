# Lab5Web - Praktikum JavaScript
Nama: Anthonius Dale Fernando
Kelas: TI 24 A1
NIM: 312410162

---

## 📋 Daftar File Praktikum

### 1. Lab 5.1 - Pengenalan JavaScript
**File:** `lab5_javascript.html`

**Tujuan:** Memahami cara menggunakan JavaScript dan output methods

**Konten:**
- Penggunaan `document.write()` untuk menulis output ke halaman HTML
- Penggunaan `console.log()` untuk menulis output ke console browser
- Penggunaan tag `<script>`

**Cara Menggunakan:**
1. Buka file `lab5_javascript.html` di browser
2. Amati output "Hello World" di halaman
3. Buka Developer Tools (F12) untuk melihat console output

---

### 2. Lab 5.2 - Alert, Method, dan Prompt
**File:** `lab5_alert_prompt.html`

**Tujuan:** Memahami berbagai cara interaksi dengan user

**Konten:**
- **Alert:** Menampilkan pesan pop-up kepada user
- **innerHTML:** Mengubah konten elemen HTML menggunakan JavaScript
- **Prompt:** Menampilkan dialog untuk input dari user

**Fungsi-Fungsi:**
- `showAlert()` - Menampilkan alert dialog
- `showMethod()` - Mengubah konten HTML dengan innerHTML
- `showPrompt()` - Meminta input nama dari user

**Contoh Penggunaan:**
```javascript
function showAlert() {
    alert("Ini adalah alert!");
}

function showMethod() {
    document.getElementById("hasil").innerHTML = "Konten berubah!";
}

let nama = prompt("Masukkan nama:");
```

---

### 3. Lab 5.3 - Pembuatan dan Pemanggilan Fungsi
**File:** `lab5_fungsi.html`

**Tujuan:** Memahami cara membuat dan memanggil fungsi

**Konten:**
- Fungsi tanpa parameter
- Fungsi dengan parameter
- Fungsi dengan return value
- Pemanggilan fungsi dari button onclick event

**Fungsi-Fungsi:**
- `sapaNama()` - Fungsi sederhana tanpa parameter
- `tambahAngka(a, b)` - Fungsi dengan 2 parameter
- `hitungPerkalian()` - Fungsi dengan return value

**Contoh Penggunaan:**
```javascript
function tambahAngka(a, b) {
    let hasil = a + b;
    document.getElementById("hasil").innerHTML = a + " + " + b + " = " + hasil;
}
```

---

### 4. Lab 5.4 - Operasi Dasar Aritmatika
**File:** `lab5_operasi_aritmatika.html`

**Tujuan:** Memahami operasi dasar aritmatika dalam JavaScript

**Konten:**
- Penjumlahan (+)
- Pengurangan (-)
- Perkalian (×)
- Pembagian (÷)
- Modulus (%)
- Validasi pembagian dengan 0

**Fitur:**
- Input field untuk memasukkan dua angka
- Tombol untuk setiap operasi aritmatika
- Error handling untuk pembagian dengan 0

**Contoh Kode:**
```javascript
function tambah() {
    let angka = getAngka();
    tampilHasil("+", angka.a + angka.b);
}

function bagi() {
    let angka = getAngka();
    if (angka.b == 0) {
        document.getElementById("hasil").innerHTML = "<b>Error: Tidak boleh dibagi 0</b>";
    } else {
        tampilHasil("÷", (angka.a / angka.b).toFixed(2));
    }
}
```

---

### 5. Lab 5.5 - Seleksi Kondisi (if..else)
**File:** `lab5_kondisi_ifelse.html`

**Tujuan:** Memahami penggunaan if..else statement

**Konten:**
- Cek bilangan positif, negatif, atau nol
- Cek nilai lulus atau tidak lulus (KKM = 70)
- Cek bilangan yang lebih besar

**Struktur if..else:**
```javascript
if (kondisi) {
    // kode jika kondisi true
} else if (kondisi2) {
    // kode jika kondisi2 true
} else {
    // kode jika semua kondisi false
}
```

**Contoh Implementasi:**
```javascript
function cekBilangan() {
    let bil = parseInt(document.getElementById("bilangan").value);
    
    if (bil > 0) {
        hasil = bil + " adalah bilangan Positif";
    } else if (bil < 0) {
        hasil = bil + " adalah bilangan Negatif";
    } else {
        hasil = bil + " adalah Nol";
    }
    
    document.getElementById("hasil1").innerHTML = hasil;
}
```

---

### 6. Lab 5.6 - Operator Switch
**File:** `lab5_switch.html`

**Tujuan:** Memahami penggunaan switch statement

**Konten:**
- Pilih hari dalam seminggu
- Pilih warna dan deskripsinya
- Pilih bulan dan jumlah harinya

**Struktur Switch:**
```javascript
switch(nilai) {
    case 1:
        // kode untuk case 1
        break;
    case 2:
        // kode untuk case 2
        break;
    default:
        // kode default
}
```

**Contoh Implementasi:**
```javascript
function pilihHari() {
    let hari = document.getElementById("hari").value;
    let nama_hari;
    
    switch(hari) {
        case "1":
            nama_hari = "Senin - Hari kerja";
            break;
        case "7":
            nama_hari = "Minggu - Akhir pekan";
            break;
        default:
            nama_hari = "Hari tidak valid";
    }
    
    document.getElementById("hasil1").innerHTML = nama_hari;
}
```

---

### 7. Lab 5.7 - Form Input dan Validasi DOM
**File:** `lab5_form_validasi.html`

**Tujuan:** Memahami manipulasi elemen HTML dan validasi form

**Konten:**
- Form input: Nama, Email, Umur, Program Studi
- Validasi pada setiap field
- Menampilkan data yang telah divalidasi
- Tombol Reset

**Validasi yang Dilakukan:**
- Nama tidak boleh kosong
- Email harus format valid (menggunakan regex)
- Umur harus antara 0-100
- Program Studi harus dipilih

**Contoh Validasi:**
```javascript
function validasiForm() {
    let nama = document.getElementById("nama").value.trim();
    
    if (nama === "") {
        document.getElementById("err_nama").style.display = "block";
        valid = false;
    }
    
    // Validasi email
    let emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    if (!emailRegex.test(email)) {
        document.getElementById("err_email").style.display = "block";
        valid = false;
    }
}
```

---

### 8. Lab 5.8 - Checkbox dengan Perhitungan Otomatis
**File:** `lab5_checkbox.html`

**Tujuan:** Memahami event handling dan DOM manipulation dengan checkbox

**Konten:**
- Menu Makanan (Nasi Goreng, Soto Ayam, Gado-Gado, Lumpia)
- Menu Minuman (Jus Jeruk, Teh Manis, Kopi)
- Menu Dessert (Es Krim, Puding)
- Perhitungan otomatis saat checkbox dicentang/dihapus
- Ringkasan pesanan dengan total harga
- Validasi minimal satu item dipilih

**Fitur Event Handler:**
```javascript
function hitungTotal() {
    let checkboxes = document.querySelectorAll('input[type="checkbox"]:checked');
    let total = 0;
    
    checkboxes.forEach(function(checkbox) {
        let harga = parseInt(checkbox.value);
        total += harga;
    });
    
    document.getElementById("total_harga").textContent = "Rp. " + total.toLocaleString('id-ID');
}
```

---

## 🎯 Tujuan Pembelajaran

Setelah menyelesaikan semua praktikum, mahasiswa diharapkan dapat:

1. ✅ Memahami sintaks dasar JavaScript
2. ✅ Memahami penggunaan JavaScript dalam web development
3. ✅ Membuat kode JavaScript sederhana
4. ✅ Memanipulasi elemen HTML dengan JavaScript
5. ✅ Membuat validasi form dengan JavaScript
6. ✅ Menggunakan event handling (onclick, onchange)
7. ✅ Menggunakan DOM API (document.getElementById, innerHTML, etc)
8. ✅ Menerapkan konsep dasar pemrograman (fungsi, kondisi, loop)

---

## 📝 Cara Menggunakan Repository

### 1. Clone Repository
```bash
git clone https://github.com/username/Lab5Web.git
cd Lab5Web
```

### 2. Buka File di Browser
Setiap file `.html` dapat dibuka langsung di browser untuk melihat hasilnya.

### 3. Validasi HTML
Validasi setiap file HTML di: http://validator.w3.org

### 4. Membaca Console
Tekan F12 untuk membuka Developer Tools dan lihat console output.

---

## 🔍 Konsep-Konsep Penting

### JavaScript Placement
- **Di tag `<head>`**: Script dijalankan sebelum halaman selesai dimuat
- **Di tag `<body>`**: Script dijalankan saat halaman dimuat
- **File eksternal**: Script dipisahkan dalam file `.js`

### Output Methods
| Method | Fungsi | Contoh |
|--------|--------|--------|
| `document.write()` | Menulis ke halaman HTML | `document.write("Hello")` |
| `innerHTML` | Mengubah konten elemen | `element.innerHTML = "Teks"` |
| `alert()` | Pop-up dialog | `alert("Pesan")` |
| `console.log()` | Output ke console | `console.log("Debug")` |

### Operator Kondisi
- **if..else**: Untuk kondisi sederhana
- **switch**: Untuk banyak kondisi dengan nilai yang sama

### Event Handlers
- `onclick`: Ketika elemen diklik
- `onchange`: Ketika nilai input berubah
- `onload`: Ketika halaman selesai dimuat







*Last Updated: 2025*
