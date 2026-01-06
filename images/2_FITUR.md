# ✨ Daftar Fitur Internal Asset Tracking

**1. Halaman Login (Seluruh Role)**

login dapat dilakukan oleh 3 role, yaitu admin,owner dan staff
<img width="1919" height="1136" alt="login" src="https://github.com/user-attachments/assets/b54a23ca-c6db-477a-87ac-55c55f08f95a" />

**2. Halaman Dashboard, Stats dan Dougnut Charts (seluruh Role)**

Seluruh role mempunyai kesempatan melihat chart dan stats dengan summary di bawah ini (nanti diperinci aja)
<img width="1917" height="1137" alt="dashboard_all_pov" src="https://github.com/user-attachments/assets/500cd6d8-15fc-4ba0-99c6-fcdd6c298320" />

**3. Navigation Sidebar versi Admin dan Owner**

Owner dan admin mempunyai tingkatan yang hampir sama. Bedanya, admin tidak dapat mengutak-atik beberapa operasional bisnis
<img width="343" height="468" alt="sidebar_admin_owner_pov" src="https://github.com/user-attachments/assets/6b4b3572-bf48-4e12-b6a0-b005cee2fe19" />

**4.Navigation Sidebar versi Staff**

Beberapa fitur diatur restricted sehingga tidak dapat diakses oleh Staff. Karena Staff berfokus pada operasional bisnis saja
<img width="295" height="434" alt="sidebar_staf_pov" src="https://github.com/user-attachments/assets/4d6ad91a-b76d-4978-ba7b-57466b661d9c" />

**5. List Motors dan Mobils di sisi Owner dan Admin**

Jadi di sisi owner bisa lakukan CRUD sementara di role lain tidak bisa. Paling kalau di staff cuman edit, view, check in check out
<img width="1919" height="1137" alt="mobils_admin_owner_pov" src="https://github.com/user-attachments/assets/b86dcf66-c1d6-4a0f-9879-51217ec1e913" />
<img width="1915" height="1136" alt="motors_owner_admin_pov" src="https://github.com/user-attachments/assets/9cf3b478-e5a6-4873-93a0-d9bf52cb8a38" />

**6. List Mobils dan Motors di sisi Staff**

Disinilah adanya check in dan check out, tapi staff tidak punya hak untuk merubah data entitas (seperti ubah nama, ubah tanggal beli, dan sebagainya)
<img width="1919" height="1138" alt="mobils_staff_pov" src="https://github.com/user-attachments/assets/4788e48a-f1a1-457e-988d-0277e8b4ec75" />

**7. Proses Check Out (form-nya)**
<img width="1919" height="1136" alt="7" src="https://github.com/user-attachments/assets/f7fde580-e569-4d33-a7fd-0bbeed027804" />

**8. Proses Check In (form-nya) Apabila kondisi Baik**
<img width="1919" height="1137" alt="8" src="https://github.com/user-attachments/assets/b54a3047-9abb-416d-a063-eb992e8cc3a4" />

**9. Proses Check In (form-nya) Apabila kondisi perlu maintenance**
<img width="1919" height="1136" alt="9" src="https://github.com/user-attachments/assets/61e64a56-4196-4c55-abf1-fd92c6dfa18f" />

**10. Maintenance di sisi Staff**

ketika ada kendaraan yang rusak masuk, di staff statusnya akan pending. Hal ini dikarenakan dibutuhkan role Owner untuk approve. dan tombol approce tersebut terlihatnya ketika login di owner. Bisa difilter berdasarkan status(aproval,rejected, pending)
<img width="1919" height="1138" alt="maintenance_staff_pov" src="https://github.com/user-attachments/assets/fc4f07a7-ef33-4426-90f5-c54d5c176103" />

**11. Maintenance di sisi Owner**

Owner bisa memilih 2 tindakan, mau aprove atau reject.
<img width="1919" height="1137" alt="maintenance_owner_pov (decide)" src="https://github.com/user-attachments/assets/65b12271-5b73-455c-9fe4-78ccc9d7d0b1" />
<img width="1919" height="1135" alt="maintenance_owner_pov (aproval-rejected)" src="https://github.com/user-attachments/assets/9be43745-5627-41ea-bb66-a0e983faeb24" />
Dan kalau misal udah selesai maintenancenya, nanti owner bisa teken complete sekaligus isi realisasi harga, dan aset akan kembali ke posisi available lagi. Tidak hanya itu, status aset yang completed akan menajdi record tetap di maintenance.

**12. Activity Log di sisi Staff, Admin dan Owner **

tidak ada CRUD di sini. Dan activity log hanya berfokus mencatat proses in out aset dari gudang (tidak mencatat pas masuk ke maintenance). Bisa difilter berdasarkan status (check in, check out,atau new data aset)
<img width="1919" height="1138" alt="activity-log_all_pov" src="https://github.com/user-attachments/assets/74c9c89b-d983-41de-aedd-144fc82c2b85" />


**13. List Owner di sisi Owner dan Admin**
<img width="1919" height="1134" alt="owners_owner_admin_pov" src="https://github.com/user-attachments/assets/cded70c9-7b49-4946-9a18-a9920417151f" />

**14. List Warehouse di sisi Owner dan Admin**
<img width="1919" height="1031" alt="warehouse_owner_pov" src="https://github.com/user-attachments/assets/43435997-11d3-4a55-97f9-64123f099731" />

**15. List Employee di sisi Owner dan Admin**
hanya admin dan onwer yang bisa CRUD, sedangkan staff tidak bisa melihat serta CRUD
<img width="1286" height="750" alt="employees_admin_owner_pov" src="https://github.com/user-attachments/assets/a6306c99-b951-4729-b323-ff7a446c3f01" />







## 🎯 PEMBAGIAN TUGAS:
**Internal Asset Tracking** merupakan sistem informasi berbasis _back-office_ yang akan menjalankan sebagian besar operasionalnya pada panel admin filament. Pembagian tugas dalam kelompok yang telah dijalankan adalah sebagai berikut:

**1. Sonia Debora Napitupulu**
   - Setup laravel & Filament ✔️
   - Management Github (Review & Merging) ✔️
   - Testing and Fixing Full Flow ✔️
   - Create fitur Charts & Stats ✔️

**2. Muhammad Naufal Isyrafi**
   - Create CRUD entitas ✔️
   - Create Migration ✔️
   - Create fitur activity log ✔️ 

**3. Ghifar Januar Abdillah**
   - fixing Activity Log ✔️ 
   - Testing CRUD ✔️
   - Testing Relation ✔️
   - Create fitur maintenance ✔️

**4. Mochammad Fadhila Putra**
   - set Role & Permission ✔️
   - create fitur Owner & Employee ✔️
   - Create Policy ✔️

**5. Mesak Mychart Elsafan Purba**
   - Implementasi Trait Activity Log ✔️
   - Staff Restriction ✔️
   - Refactoring Status Logic ✔️
   - Deployment ✔️

**6. Rifky Cahyo Putra**
   - Laporan ✔️
   - Figma Design ✔️ 
   - ERD ✔️
