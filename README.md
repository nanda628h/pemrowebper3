# Praktikum 3: HTML Lanjutan - List, Table, dan Form

## 📝 Data Mahasiswa
- **Nama**: ananda Friezy Eka Cahya
- **NIM**: 312410151
- **Kelas**: TI 24 A1    
- **Mata Kuliah**: Pemrograman Web

---

## 📚 Tujuan Praktikum
1. Memahami struktur dasar pembuatan List (Ordered, Unordered, Description)
2. Memahami struktur dasar pembuatan Tabel
3. Memahami tag-tag dasar pembuatan Form
4. Mampu membuat dokumen HTML yang lebih kompleks
5. Mengimplementasikan penggunaan CSS pada List, Table dan Form

---

## 🎯 Langkah-langkah Praktikum

### 1. Membuat HTML List

#### 1.1 Ordered List (Daftar Berurutan)

**Kode HTML:**
```html
<ol>
    <li>Pemrograman Web</li>
    <li>Sistem Informasi</li>
    <li>Basis Data 2</li>
</ol>
```

**Penjelasan:**
- Tag `<ol>` digunakan untuk membuat ordered list (daftar terurut)
- Tag `<li>` digunakan untuk setiap item dalam list
- Secara default, ordered list menggunakan angka 1, 2, 3, dst

---

#### 1.2 Ordered List dengan Atribut Type

**Kode HTML:**
```html
<!-- Type A (Huruf Besar) -->
<ol type="A">
    <li>Pemrograman Web</li>
    <li>Sistem Informasi</li>
    <li>Rekayasa Perangkat Lunak</li>
</ol>

<!-- Type a (Huruf Kecil) -->
<ol type="a">
    <li>Pemrograman Web</li>
    <li>Sistem Informasi</li>
    <li>Rekayasa Perangkat Lunak</li>
</ol>

<!-- Type I (Romawi Besar) -->
<ol type="I">
    <li>Pemrograman Web</li>
    <li>Sistem Informasi</li>
    <li>Rekayasa Perangkat Lunak</li>
</ol>

<!-- Type i (Romawi Kecil) -->
<ol type="i">
    <li>Pemrograman Web</li>
    <li>Sistem Informasi</li>
    <li>Rekayasa Perangkat Lunak</li>
</ol>

<!-- Dengan atribut start -->
<ol type="A" start="4">
    <li>Pemrograman Web</li>
    <li>Sistem Informasi</li>
    <li>Rekayasa Perangkat Lunak</li>
</ol>
```

**Penjelasan:**
- Atribut `type` mengubah jenis penomoran
- `type="A"` = A, B, C, ...
- `type="a"` = a, b, c, ...
- `type="I"` = I, II, III, ...
- `type="i"` = i, ii, iii, ...
- Atribut `start` menentukan nilai awal penomoran

---

#### 1.3 Unordered List (Daftar Tidak Berurutan)

**Kode HTML:**
```html
<ul type="square">
    <li>Jaringan Komputer</li>
    <li>Struktur Data</li>
    <li>Algoritma &amp; Pemrograman</li>
</ul>
```

**Penjelasan:**
- Tag `<ul>` digunakan untuk unordered list (daftar tidak terurut)
- Atribut `type` bisa: `disc` (default), `circle`, `square`, `none`

---

#### 1.4 Description List

**Kode HTML:**
```html
<dl>
    <dt>Fakultas Teknik</dt>
    <dd>Teknik Industri</dd>
    <dd>Teknik Informatika</dd>
    <dd>Teknik Lingkungan</dd>
    <dt>Fakultas Ekonomi dan Bisnis</dt>
    <dd>Akuntansi</dd>
    <dd>Manajemen</dd>
    <dd>Bisnis Digital</dd>
</dl>
```

**Penjelasan:**
- `<dl>` = Description List (daftar deskripsi)
- `<dt>` = Description Term (istilah/judul)
- `<dd>` = Description Definition (penjelasan/isi)

---

#### 1.5 Nested List

**Kode HTML:**
```html
<ul>
    <li>Makanan
        <ol>
            <li>Nasi Padang</li>
            <li>Ayam Bakar</li>
            <li>Rendang</li>
        </ol>
    </li>
    <li>Minuman
        <ol>
            <li>Jus Mangga</li>
            <li>Es Teh</li>
            <li>Kopi</li>
        </ol>
    </li>
</ul>
```

**Penjelasan:**
- List dapat dibuat di dalam list lain (nested list)
- Berguna untuk membuat struktur hierarki

---

### 2. Membuat HTML Table

#### 2.1 Tabel Sederhana

**Kode HTML:**
```html
<table border="1" cellpadding="4" cellspacing="0">
    <thead>
        <tr>
            <th>No.</th>
            <th>Fakultas</th>
            <th>Program Studi</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1.</td>
            <td>Teknik</td>
            <td>Teknik Informatika</td>
        </tr>
        <tr>
            <td>2.</td>
            <td>Teknik</td>
            <td>Teknik Industri</td>
        </tr>
        <tr>
            <td>3.</td>
            <td>Teknik</td>
            <td>Teknik Lingkungan</td>
        </tr>
    </tbody>
</table>
```

**Penjelasan:**
- `<table>` = tag utama untuk membuat tabel
- `<thead>` = bagian header tabel
- `<tbody>` = bagian body tabel
- `<tr>` = table row (baris)
- `<th>` = table header (kolom header)
- `<td>` = table data (kolom data)
- `border` = ketebalan border
- `cellpadding` = jarak antara border dengan konten
- `cellspacing` = jarak antar sel

---

#### 2.2 Eksperimen Cellpadding dan Cellspacing

**Kode HTML:**
```html
<!-- Cellpadding = 0, Cellspacing = 0 -->
<table border="1" cellpadding="0" cellspacing="0">
    ...
</table>

<!-- Cellpadding = 10, Cellspacing = 0 -->
<table border="1" cellpadding="10" cellspacing="0">
    ...
</table>

<!-- Cellpadding = 5, Cellspacing = 5 -->
<table border="1" cellpadding="5" cellspacing="5">
    ...
</table>
```
**Penjelasan:**
- **Cellpadding**: Mengatur jarak antara border sel dengan konten di dalamnya
- **Cellspacing**: Mengatur jarak antar sel tabel

---

#### 2.3 Tabel dengan Rowspan (Penggabungan Vertikal)

**Kode HTML:**
```html
<table border="1" cellpadding="6" cellspacing="0">
    <thead>
        <tr>
            <th>No.</th>
            <th>Fakultas</th>
            <th>Program Studi</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1.</td>
            <td rowspan="3">Teknik</td>
            <td>Teknik Informatika</td>
        </tr>
        <tr>
            <td>2.</td>
            <td>Teknik Industri</td>
        </tr>
        <tr>
            <td>3.</td>
            <td>Teknik Lingkungan</td>
        </tr>
    </tbody>
</table>
```

**Penjelasan:**
- Atribut `rowspan` digunakan untuk menggabungkan sel secara VERTIKAL
- `rowspan="3"` = menggabungkan 3 baris

---

#### 2.4 Tabel dengan Colspan (Penggabungan Horizontal)

**Kode HTML:**
```html
<table border="1" cellpadding="6" cellspacing="0">
    <thead>
        <tr>
            <th colspan="3">Data Mahasiswa</th>
        </tr>
        <tr>
            <th>No.</th>
            <th>Nama</th>
            <th>Jurusan</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>1.</td>
            <td>Budi</td>
            <td>Teknik Informatika</td>
        </tr>
        <tr>
            <td>2.</td>
            <td>Ani</td>
            <td>Sistem Informasi</td>
        </tr>
        <tr>
            <td colspan="3" style="text-align: center;">Total: 2 Mahasiswa</td>
        </tr>
    </tbody>
</table>
```

**Penjelasan:**
- Atribut `colspan` digunakan untuk menggabungkan sel secara HORIZONTAL
- `colspan="3"` = menggabungkan 3 kolom

---

#### 2.5 Tabel Kompleks (Kombinasi Rowspan & Colspan)

**Kode HTML:**
```html
<table border="1" cellpadding="8" cellspacing="0">
    <tr>
        <td colspan="2">Baris 1 kolom 1 (Colspan=2)</td>
    </tr>
    <tr>
        <td>Baris 2 kolom 1</td>
        <td>Baris 2 kolom 2</td>
    </tr>
    <tr>
        <td>Baris 3 kolom 1</td>
        <td>Baris 3 kolom 2</td>
    </tr>
    <tr>
        <td rowspan="2">Baris 4 kolom 1 (Rowspan=2)</td>
        <td>Baris 4 kolom 2</td>
    </tr>
    <tr>
        <td>Baris 5 kolom 2</td>
    </tr>
</table>
```

**Penjelasan:**
- Kombinasi `rowspan` dan `colspan` untuk membuat tabel yang lebih kompleks

---

### 3. Membuat HTML Form

#### 3.1 Form Login Sederhana

**Kode HTML:**
```html
<form action="proses.php" method="post">
    <fieldset>
        <legend>Login</legend>
        <p>
            <label for="uname">Username</label>
            <input type="text" id="uname" name="username">
        </p>
        <p>
            <label for="passwd">Password</label>
            <input type="password" id="passwd" name="password">
        </p>
        <p><input type="submit" value="Login"></p>
    </fieldset>
</form>
```

**Penjelasan:**
- `<form>` = tag utama untuk membuat form
- `action` = URL tujuan pengiriman data
- `method` = metode pengiriman (GET/POST)
- `<fieldset>` = mengelompokkan elemen form
- `<legend>` = judul untuk fieldset
- `<label>` = label untuk input
- `<input>` = elemen input

---

#### 3.2 Form dengan CSS

**Kode HTML:**
```html
<style>
form p > label {
    display: inline-block;
    width: 100px;
}
form input[type="text"], 
form input[type="password"],
form textarea {
    border: 1px solid #197a43;
}
form input[type="submit"] {
    border: 1px solid #197a43;
    background-color: #197a43;
    color: #ffffff;
    font-weight: bold;
    padding: 5px 15px;
}
</style>

<form action="proses.php" method="post">
    <fieldset>
        <legend>Data Pelanggan</legend>
        <p>
            <label for="nama">Nama</label>
            <input type="text" id="nama" name="nama">
        </p>
        <p>
            <label for="alamat">Alamat</label>
            <textarea id="alamat" name="alamat" cols="30" rows="4"></textarea>
        </p>
        <p>
            <label>Jenis Kelamin</label>
            <input id="jk_l" type="radio" name="kelamin" value="L" />
            <label for="jk_l">Laki-laki</label>
            <input id="jk_p" type="radio" name="kelamin" value="P" />
            <label for="jk_p">Perempuan</label>
        </p>
        <p><input type="submit" value="Simpan"></p>
    </fieldset>
</form>
```

**Penjelasan:**
- CSS digunakan untuk mempercantik tampilan form
- `display: inline-block` membuat label sejajar
- Border dan warna disesuaikan

---

### 4. Tugas: Dropdown Menu & Multiple Selection

#### 4.1 Dropdown Menu (Single Selection)

**Kode HTML:**
```html
<label for="fakultas">Fakultas</label>
<select id="fakultas" name="fakultas">
    <option value="">-- Pilih Fakultas --</option>
    <option value="teknik">Fakultas Teknik</option>
    <option value="ekonomi">Fakultas Ekonomi dan Bisnis</option>
    <option value="hukum">Fakultas Hukum</option>
</select>
```
**Penjelasan:**
- Tag `<select>` untuk membuat dropdown
- Tag `<option>` untuk setiap pilihan
- Hanya bisa memilih SATU opsi

---

#### 4.2 Dropdown dengan Optgroup

**Kode HTML:**
```html
<label for="prodi">Program Studi</label>
<select id="prodi" name="prodi">
    <option value="">-- Pilih Program Studi --</option>
    <optgroup label="Fakultas Teknik">
        <option value="ti">Teknik Informatika</option>
        <option value="si">Sistem Informasi</option>
        <option value="te">Teknik Elektro</option>
    </optgroup>
    <optgroup label="Fakultas Ekonomi">
        <option value="akuntansi">Akuntansi</option>
        <option value="manajemen">Manajemen</option>
    </optgroup>
</select>
```

**Penjelasan:**
- `<optgroup>` mengelompokkan opsi berdasarkan kategori
- Membuat dropdown lebih terorganisir

---

#### 4.3 Multiple Selection Listbox

**Kode HTML:**
```html
<label for="matakuliah">Mata Kuliah Pilihan</label>
<select id="matakuliah" name="matakuliah[]" multiple size="8">
    <option value="web">Pemrograman Web</option>
    <option value="mobile">Pemrograman Mobile</option>
    <option value="database">Basis Data Lanjut</option>
    <option value="ai">Artificial Intelligence</option>
    <option value="iot">Internet of Things</option>
    <option value="cyber">Cyber Security</option>
    <option value="cloud">Cloud Computing</option>
    <option value="data">Data Science</option>
    <option value="blockchain">Blockchain</option>
    <option value="game">Game Development</option>
</select>
```

**Penjelasan:**
- Atribut `multiple` memungkinkan memilih BANYAK opsi
- Atribut `size` menentukan jumlah baris yang ditampilkan
- Name menggunakan `[]` untuk mengirim data sebagai array
- **Cara menggunakan**: Tahan CTRL (Windows) atau CMD (Mac) sambil klik untuk memilih beberapa item

---

#### 4.4 Screenshot Multiple Selection (Beberapa Item Terpilih)


**Penjelasan:**
- Screenshot menunjukkan beberapa item yang sudah dipilih
- Item yang dipilih akan ter-highlight

---

## 📊 Perbandingan Single vs Multiple Selection

| Aspek | Single Selection | Multiple Selection |
|-------|------------------|-------------------|
| Tag | `<select>` | `<select multiple>` |
| Atribut | Tanpa `multiple` | Dengan `multiple` |
| Jumlah Pilihan | 1 opsi saja | Banyak opsi |
| Name | `name="field"` | `name="field[]"` |
| Cara Memilih | Klik biasa | CTRL/CMD + Klik |
| Tampilan | Dropdown | Listbox |
| Size | Opsional | Direkomendasikan |

---

## 🎨 Pertanyaan dan Jawaban

### 1. Perbedaan `h1 {...}` dengan `#intro h1 {...}`

**Jawaban:**

- **`h1 {...}`** 
  - Selector **elemen** yang menargetkan **SEMUA elemen h1** di seluruh halaman
  - Spesifisitas: 0,0,0,1

- **`#intro h1 {...}`**
  - Selector **descendant** yang hanya menargetkan **elemen h1 yang berada di dalam elemen dengan id="intro"**
  - Spesifisitas: 0,1,0,1 (lebih tinggi)

**Contoh:**
```html
<h1>Judul 1</h1> <!-- Terkena h1 {...} -->

<div id="intro">
    <h1>Judul 2</h1> <!-- Terkena h1 {...} DAN #intro h1 {...} -->
</div>

<h1>Judul 3</h1> <!-- Terkena h1 {...} -->
```

Jika ada konflik styling, `#intro h1` akan menang karena spesifisitas lebih tinggi.

---

### 2. Prioritas CSS: Internal vs Eksternal vs Inline

**Jawaban:**

**Urutan Prioritas (dari tertinggi ke terendah):**
1. **Inline CSS** (langsung di elemen) - PRIORITAS TERTINGGI
2. **Internal/Eksternal CSS** (tergantung mana yang ditulis terakhir)
3. Browser default

**Yang ditampilkan:** **Inline CSS** akan selalu menang!

**Contoh:**
```html
<!-- CSS Eksternal -->
<style>
.box {
    background-color: blue;
    color: white;
}
</style>

<!-- CSS Internal -->
<style>
.box {
    background-color: green;
    color: yellow;
}
</style>

<!-- Hasilnya -->
<div class="box">
    Background: GREEN, Color: YELLOW (Internal CSS menang karena ditulis terakhir)
</div>

<div class="box" style="background-color: red; color: white;">
    Background: RED, Color: WHITE (Inline CSS SELALU menang!)
</div>
```

**Kesimpulan:**
- Inline CSS memiliki prioritas tertinggi
- Jika tidak ada inline, CSS yang ditulis terakhir yang akan diterapkan
- Properti yang tidak didefinisikan di tingkat lebih tinggi akan mengambil dari tingkat di bawahnya

---

### 3. Prioritas ID vs Class Selector

**Jawaban:**

**Yang ditampilkan:** **ID Selector** akan selalu menang!

**Spesifisitas:**
- **ID selector** (#paragraf-1): 0,1,0,0 = 100
- **Class selector** (.text-paragraf): 0,0,1,0 = 10

**Contoh:**
```html
<style>
/* CLASS SELECTOR */
.text-paragraf {
    color: blue;
    background-color: lightblue;
    font-size: 16px;
}

/* ID SELECTOR */
#paragraf-1 {
    color: red;
    background-color: lightyellow;
    font-size: 20px;
}
</style>

<p id="paragraf-1" class="text-paragraf">
    Warna teks: MERAH (dari ID)
    Background: LIGHTYELLOW (dari ID)
    Font-size: 20px (dari ID)
    ID SELECTOR MENANG!
</p>
```
