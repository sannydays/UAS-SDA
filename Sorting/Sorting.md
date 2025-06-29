
## 1. 🫧 Bubble Sort

### 📌 Penjelasan:
Membandingkan pasangan elemen bersebelahan dan menukarnya jika urutannya salah. Elemen terbesar "menggelembung" ke akhir.

### 💻 Kode Java:
```java
void bubbleSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

### 📊 Kompleksitas:
- Waktu (Best): O(n) – jika sudah terurut
- Waktu (Average & Worst): O(n²)
- Ruang: O(1)

---

## 2. 🔧 Insertion Sort

### 📌 Penjelasan:
Menyisipkan elemen ke posisi yang tepat pada bagian array yang sudah terurut.

### 💻 Kode Java:
```java
void insertionSort(int[] arr) {
    for (int i = 1; i < arr.length; i++) {
        int key = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = key;
    }
}
```

### 📊 Kompleksitas:
- Waktu (Best): O(n) – jika hampir terurut
- Waktu (Average & Worst): O(n²)
- Ruang: O(1)

---

## 3. 🔁 Selection Sort

### 📌 Penjelasan:
Memilih elemen terkecil dari bagian yang belum terurut, lalu menukarnya ke posisi yang benar.

### 💻 Kode Java:
```java
void selectionSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        int minIdx = i;
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIdx]) {
                minIdx = j;
            }
        }
        int temp = arr[minIdx];
        arr[minIdx] = arr[i];
        arr[i] = temp;
    }
}
```

### 📊 Kompleksitas:
- Waktu (Best, Avg, Worst): O(n²)
- Ruang: O(1)

---

## 4. 🧩 Merge Sort

### 📌 Penjelasan:
Menggunakan metode divide and conquer. Array dibagi dua, masing-masing disortir, lalu digabung kembali.

### 💻 Kode Java:
```java
void mergeSort(int[] arr, int left, int right) {
    if (left < right) {
        int mid = (left + right) / 2;
        mergeSort(arr, left, mid);
        mergeSort(arr, mid + 1, right);
        merge(arr, left, mid, right);
    }
}

void merge(int[] arr, int left, int mid, int right) {
    int n1 = mid - left + 1;
    int n2 = right - mid;

    int[] L = new int[n1];
    int[] R = new int[n2];

    for (int i = 0; i < n1; i++)
        L[i] = arr[left + i];
    for (int j = 0; j < n2; j++)
        R[j] = arr[mid + 1 + j];

    int i = 0, j = 0, k = left;
    while (i < n1 && j < n2) {
        if (L[i] <= R[j]) {
            arr[k++] = L[i++];
        } else {
            arr[k++] = R[j++];
        }
    }

    while (i < n1) arr[k++] = L[i++];
    while (j < n2) arr[k++] = R[j++];
}
```

### 📊 Kompleksitas:
- Waktu (Best, Avg, Worst): O(n log n)
- Ruang: O(n) – karena menggunakan array tambahan

---

## 📌 Catatan Tambahan:
| Algoritma     | In-Place? | Stabil? | Cocok untuk |
|---------------|-----------|---------|--------------|
| Bubble Sort   | ✅ Ya     | ✅ Ya   | Data kecil, belajar dasar |
| Insertion Sort| ✅ Ya     | ✅ Ya   | Data hampir terurut |
| Selection Sort| ✅ Ya     | ❌ Tidak| Gak terlalu efisien |
| Merge Sort    | ❌ Tidak  | ✅ Ya   | Data besar (stabil dan cepat) |
