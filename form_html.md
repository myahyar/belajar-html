# Form HTML

Form HTML digunakan untuk mengumpulkan data dari pengguna. Data ini dapat dikirim ke server untuk diproses.

## Elemen Dasar Form

```html
<form action="proses.php" method="POST">
    <label for="nama">Nama:</label>
    <input type="text" id="nama" name="nama" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <label for="password">Password:</label>
    <input type="password" id="password" name="password" required>

    <input type="submit" value="Kirim">
</form>
```

## Atribut Penting dalam `<form>`

- **action**: Menentukan URL tujuan data dikirim.
- **method**: Metode pengiriman (`GET` atau `POST`).
- **target**: Menentukan jendela tujuan (`_self`, `_blank`, dll.).
- **enctype**: Digunakan saat mengunggah file.

## Jenis Input dalam Form

```html
<input type="text" name="nama">
<input type="email" name="email">
<input type="password" name="password">
<input type="radio" name="gender" value="L"> Laki-laki
<input type="radio" name="gender" value="P"> Perempuan
<input type="checkbox" name="hobi" value="Membaca"> Membaca
<input type="checkbox" name="hobi" value="Olahraga"> Olahraga
<input type="file" name="file">
<input type="submit" value="Kirim">
```

## Validasi Input

### Validasi HTML5

```html
<input type="text" name="nama" required minlength="3" maxlength="20">
<input type="email" name="email" required>
<input type="number" name="usia" min="18" max="60">
```

### Validasi dengan JavaScript

```html
<script>
    function validasiForm() {
        let nama = document.getElementById("nama").value;
        if (nama.length < 3) {
            alert("Nama harus lebih dari 2 karakter");
            return false;
        }
        return true;
    }
</script>
<form onsubmit="return validasiForm()">
    <input type="text" id="nama" name="nama" required>
    <input type="submit" value="Kirim">
</form>
```

## Select dan Textarea

```html
<select name="kota">
    <option value="jakarta">Jakarta</option>
    <option value="bandung">Bandung</option>
</select>

<textarea name="pesan" rows="4" cols="30"></textarea>
```

## Contoh Lengkap Form

```html
<form action="submit.php" method="POST">
    <fieldset>
        <legend>Form Registrasi</legend>

        <label for="nama">Nama:</label>
        <input type="text" id="nama" name="nama" required>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required>

        <label for="gender">Jenis Kelamin:</label>
        <input type="radio" name="gender" value="L"> Laki-laki
        <input type="radio" name="gender" value="P"> Perempuan

        <label for="hobi">Hobi:</label>
        <input type="checkbox" name="hobi" value="Membaca"> Membaca
        <input type="checkbox" name="hobi" value="Olahraga"> Olahraga

        <label for="kota">Kota:</label>
        <select name="kota">
            <option value="jakarta">Jakarta</option>
            <option value="bandung">Bandung</option>
        </select>

        <label for="pesan">Pesan:</label>
        <textarea name="pesan" rows="4" cols="30"></textarea>

        <input type="submit" value="Daftar">
    </fieldset>
</form>
```

## Kesimpulan

Form HTML memungkinkan interaksi pengguna dengan aplikasi web. Dengan menggunakan atribut HTML dan validasi, kita dapat memastikan data yang dikirim sesuai dengan kebutuhan.
