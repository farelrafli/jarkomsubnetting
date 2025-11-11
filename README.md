Deskripsi Tugas

Tugas ini merupakan implementasi konsep Subnetting (VLSM & CIDR) pada topologi jaringan dengan pembagian IP yang efisien.
Konfigurasi dibuat dan diuji menggunakan Cisco Packet Tracer, dengan hasil akhir berupa tabel subnetting, CIDR, supernetting, serta file .pkt konfigurasi lengkap.

 Tujuan

Memahami dan menerapkan konsep VLSM (Variable Length Subnet Mask).

Menerapkan CIDR (Classless Inter-Domain Routing) untuk penggabungan subnet.

Melakukan Supernetting sebagai penyederhanaan jaringan tingkat lanjut.

Mengonfigurasi IP address di setiap perangkat pada topologi menggunakan Cisco Packet Tracer.
<img width="959" height="316" alt="Screenshot 2025-11-11 194435" src="https://github.com/user-attachments/assets/767a39c1-c560-4293-ab2b-cb1782efcef2" />

 Topologi



 Hasil Perhitungan
 Tabel VLSM
Network Name	Required Hosts	Network	Prefix	Mask	Host Range	Broadcast	Gateway
Sekretariat	380	10.115.0.0	/23	255.255.254.0	10.115.0.1 - 10.115.1.254	10.115.1.255	10.115.0.1
Kurikulum	220	10.115.2.0	/24	255.255.255.0	10.115.2.1 - 10.115.2.254	10.115.2.255	10.115.2.1
Bidang Guru & Tendik	95	10.115.3.0	/25	255.255.255.128	10.115.3.1 - 10.115.3.126	10.115.3.127	10.115.3.1
Sarana Prasarana	45	10.115.3.128	/26	255.255.255.192	10.115.3.129 - 10.115.3.190	10.115.3.191	10.115.3.129
Pengawas Sekolah (Pusat)	18	10.115.3.192	/27	255.255.255.224	10.115.3.193 - 10.115.3.222	10.115.3.223	10.115.3.193
Pengawas Sekolah (Cabang)	18	10.115.3.224	/27	255.255.255.224	10.115.3.225 - 10.115.3.254	10.115.3.255	10.115.3.225
Server & Admin	6	10.115.4.0	/29	255.255.255.248	10.115.4.1 - 10.115.4.6	10.115.4.7	10.115.4.1
Link Router	2	10.115.4.8	/30	255.255.255.252	10.115.4.9 - 10.115.4.10	10.115.4.11	10.115.4.9
 Tabel CIDR
Network Group	Network	Prefix	Mask	Host Range	Keterangan
Central LANs (agg)	10.115.0.0	/22	255.255.252.0	10.115.0.0 – 10.115.3.255	Gabungan Sekretariat, Kurikulum, Guru, Sarpras, Pengawas
Servers	10.115.4.0	/29	255.255.255.248	10.115.4.0 – 10.115.4.7	Server & Admin
Router Link	10.115.4.8	/30	255.255.255.252	10.115.4.8 – 10.115.4.11	Router-to-Router
 Supernetting
Supernet Name	Networks Digabung	Supernet Address	Prefix	Mask	Range Host	Broadcast	Total Host
Supernet A (Keseluruhan Jaringan)	Central LANs + Servers + Router Link	10.115.0.0	/21	255.255.248.0	10.115.0.1 – 10.115.7.254	10.115.7.255	2048
 File yang Disertakan


Kesimpulan

Pembagian IP berhasil dilakukan dengan metode VLSM untuk efisiensi alamat.

Penggabungan jaringan dilakukan menggunakan CIDR.

Supernetting /21 mencakup seluruh jaringan organisasi.

Seluruh konfigurasi diverifikasi melalui Cisco Packet Tracer dan berfungsi dengan baik.
