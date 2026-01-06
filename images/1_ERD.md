# 📦 Internal Asset Tracking System

## 📖 Deskripsi
Sistem **Internal Asset Tracking** dirancang untuk memantau dan mengelola aset perusahaan, termasuk kendaraan (mobil dan motor), gudang penyimpanan, aktivitas perpindahan aset, serta proses perawatan. Sistem ini juga menghubungkan aset dengan karyawan yang bertanggung jawab.

---

## 🗂️ Entity Relationship Diagram (ERD)

### Entitas Utama
1. **Employees**
   - PK: `id`
   - Atribut: email (O), no_telp (O), foto (O), nama (O), update_at, create_at

2. **Mobil**
   - PK: `id`
   - FK: `current_holder_id` → employees.id  
   - FK: `warehouse_id` → warehouses.id  
   - Atribut: merek_mobil (O), rencana_kembali (O), tanggal_beli (O), tahun_keluaran (O), status, tipe_mobil (O), plat_nomor (O), update_at, created_at

3. **Motor**
   - PK: `id`
   - FK: `current_holder_id` → employees.id  
   - FK: `warehouse_id` → warehouses.id  
   - Atribut: merek_motor (O), tipe_motor (O), plat_motor (O), rencana_kembali (O), tanggal_beli (O), tahun_keluaran (O), status, update_at, created_at

4. **Warehouses**
   - PK: `id`
   - Atribut: pic (O), nama_gudang (O), alamat (O), update_at, created_at

5. **Maintenance / Maintenances**
   - PK: `id`
   - FK: `employee_id` → employees.id  
   - FK: `asset_id` → mobil.id / motor.id (via asset_type)  
   - Atribut: approval, tanggal_selesai (O), deskripsi (O), biaya (O), update_at, created_at

6. **Activity Logs**
   - PK: `id`
   - FK: `employee_id` → employees.id  
   - FK: `old_location_id`, `new_location_id` → warehouses.id  
   - FK: `asset_id` → mobil.id / motor.id (via asset_type)  
   - Atribut: keterangan, created_at, updated_at, update_at

---

## 🔗 Relasi Antar Entitas

### One-to-Many
- Employees → Mobil (satu karyawan bisa memegang banyak mobil)  
- Employees → Motor (satu karyawan bisa memegang banyak motor)  
- Employees → Maintenance (satu karyawan bisa menangani banyak perawatan)  
- Warehouses → Mobil/Motor (satu gudang bisa menyimpan banyak kendaraan)  
- Warehouses → Activity Logs (satu gudang bisa menjadi lokasi asal/tujuan banyak aktivitas)

### Many-to-One
- Mobil → Employees (banyak mobil bisa dipegang oleh satu karyawan)  
- Motor → Employees (banyak motor bisa dipegang oleh satu karyawan)  
- Mobil/Motor → Warehouses (banyak kendaraan bisa disimpan di satu gudang)  
- Maintenance → Employees (banyak perawatan bisa dilakukan oleh satu karyawan)

---

## ⚙️ Catatan Tambahan
- Atribut bertanda **(O)** bersifat opsional.  
- `asset_type` digunakan untuk membedakan jenis aset (mobil atau motor).  
- Terdapat duplikasi entitas **maintenance** dan **maintenances** yang sebaiknya dikonsolidasi.  

---

## ✅ Kesimpulan
ERD ini memberikan gambaran menyeluruh tentang bagaimana aset internal perusahaan dikelola, dilacak, dan dirawat. Struktur relasi antar entitas mendukung pelacakan tanggung jawab, lokasi, dan histori aktivitas aset secara sistematis.
