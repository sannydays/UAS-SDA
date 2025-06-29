## Pengertian Hash Function?
Hash Function adalah **fungsi yang mengubah data** (seperti string, angka, objek) menjadi sebuah **angka unik tetap** yang disebut *hash*.

Biasanya digunakan untuk **menentukan posisi data** di dalam struktur data seperti array, agar proses pencarian dan penyimpanan jadi **lebih cepat**.

---

## Tujuan / Kegunaan
- **Mempercepat akses data** (pencarian hampir O(1))
- Menyimpan data berdasarkan **kunci unik**
- Digunakan dalam:
  - `HashMap`, `HashSet`
  - Hash Table
  - Login/password hashing
  - Indexing database
  - Kompilator, caching, blockchain

---

## ⚙️ Contoh Sederhana
```java
int hash(String key) {
    int sum = 0;
    for (int i = 0; i < key.length(); i++) {
        sum += key.charAt(i);
    }
    return sum % arraySize;
}
