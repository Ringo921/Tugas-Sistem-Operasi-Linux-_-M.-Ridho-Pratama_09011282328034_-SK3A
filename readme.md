Nama  : M.Ridho Pratama

Kelas  : SK3A

NIM    : 09011282328034

Tugas Sistem Operasi Mengubah Port SSH default ke Port 40



Untuk melihat Port ssh yang digunakan sekarang kita bisa menggunakan command berikut:

systemctl status ssh

![Screenshot 2024-10-29 234729](https://github.com/user-attachments/assets/6f7c25bc-76a3-43c6-86d1-f52fd7560220)

Pada gambar tersebut menampilkan bahwa Port masih menggunakan Port bawaan atau Port 22 

Dan untuk mengganti Port bawaan tersebut ke Port yang kita mau (Port 40) kita bisa menggunakan command berikut

sudo nano /etc/ssh/ssh_config

![Screenshot 2024-10-29 233604](https://github.com/user-attachments/assets/627403d4-d1d3-4915-b38a-bd0f87995f27)

Dan akan menampilkan tampilan seperti berikut

![Screenshot 2024-10-29 234809](https://github.com/user-attachments/assets/a097db33-3b78-4312-9c88-41f86a2386b5)

Dan untuk mengubah Port bawaan tersebut ke Port yang kita mau. Kita bisa mengganti Port 22 ke Port 40. Tidak lupa hastagnya dihapus. Kemudian untuk menyimpan perubahan yang telah kita lakukan, kita bisa menggunakan "Ctrl + O" atau "Ctrl + S" untuk menyimpan. Dan untuk keluar dari tampilan GNU Nano kita bisa menggunakan "Ctrl + x" 

![Screenshot 2024-10-29 235132](https://github.com/user-attachments/assets/d945364f-57f9-4aed-b9d5-fb14272f28d5)

Dan untuk menerapkan perubahan yang telah dilakukan, kita bisa menggunakan
ufw allow 40/tcp
ufw enable

![Screenshot 2024-10-30 000019](https://github.com/user-attachments/assets/2cb46349-872d-4adb-b48a-861615f75d13)

Terakhir. Untuk melihat status ufw kita bisa menggunakan

ufw status

![Screenshot 2024-10-30 000033](https://github.com/user-attachments/assets/1c6a2737-f644-47c2-b292-e24385607d08)
