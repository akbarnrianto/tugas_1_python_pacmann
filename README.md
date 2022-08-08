# tugas_1_python_pacmann

## Tujuan Pengerjaan Tugas
Mengimplementasikan Pembelajaran Dasar Python :
1. Basic Operation untuk Variables dan String
2. Melakukan Branching/Conditional yaitu Boolean Operation, Conditionalsm Nested Conditionals
3. Melakukan Looping While, For, dan Loop with Conditionals

## Berikut pertanyaan dan penyelesaian yang dilakukan (untuk hasil output bisa melihat langsung file .ipynb tersebut)
Sebuah penelitian mengenai bakteri B dilakukan oleh beberapa ilmuwan. Melalui penelitian tersebut diketahui bahwa bakteri B akan menggandakan diri setiap jam. Dibuat simulasi dengan pengaturan sebagai berikut:
<ol>
    <li>Jumlah awal bakteri B adalah 256</li>
    <li>Bakteri dibiarkan selama 11 jam</li>
    <li>Dihitung jumlah akhir bakteri</li>
</ol>
Buatlah program untuk membantu simulasi tersebut

Penyelesaian :
1. Coba lakukanlah perhitungan sederhana untuk menghitung 256 x 2.
``` 
jawaban_2 = 256 * 2 # Tuliskan jawabanmu di sini
print(jawaban_2)
```

2. Kalikanlah jawaban tadi dengan 2 dan simpan di variabel jawaban_2
```
jawaban_2 = jawaban_2 * 2 # Tuliskan jawabanmu di sini
print(jawaban_2)
```

3. Kalikanlah jawaban tadi dengan 2 dan simpan di variabel jawaban_2, namun gunakan Augmented Arithmetic Assignments.
```
jawaban_2 *= 2 # Tuliskan jawabanmu di sini
print(jawaban_2)
```

4. Dari nomor 1 sampai 3, telah dilakukan perkalian 256 x 2 x 2 x 2. Coba lakukan hal yang sama tapi menggunakan for loop
```
jawaban_5 = 256
for i in range(3): # Tentukan range yang sesuai
    jawaban_5 *= 2 # Gunakan Augmented Arithmetic Assignments
    
print(jawaban_5)
```

5. Mirip dengan nomor 4, namun gunakan while loop dengan kondisi jika jawaban sudah lebih dari 10.000 maka perkalian akan berhenti
```
jawaban_6 = 256
while jawaban_6 < 10000: # Isikan kondisi yang sesuai
    jawaban_6 *= 2 # Gunakan Augmented Arithmetic Assignments
print(jawaban_6)
```

6. Kembali ke soal bakteri, coba buat program simulasi tersebut
```
jumlah_bakteri = 256
# kode anda
for i in range(11):
    jumlah_bakteri *= 2
print(jumlah_bakteri)
```

7. Setelah menggandakan diri setiap jam, jika ditambahkan kondisi bahwa setiap 3 jam, 1/3 bakterinya akan mati, Berapa jumlah bakteri akhir?
```
jumlah_bakteri = 256
# kode anda
for i in range(1,12):
    jumlah_bakteri *= 2
    if i % 3 == 0:
        jumlah_bakteri = int(jumlah_bakteri - ((1/3)*jumlah_bakteri))
print(jumlah_bakteri)
```

Berikut adalah pertanyaan untuk String Method :
9. Sebuah bioskop ingin memutar film dan menampilkan judul film tersebut di website mereka. Namun judul film tersebut semuanya memakai huruf kecil. Bantulah bioskop tersebut menampilkan dengan format judul:
The Lord Of The Rings: The Return Of The King
```
judul = 'the lord of the rings: the return of the king'
jawaban_9 =  judul.title() #tulis code di sini
print(jawaban_9)
```

10. Carilah ada berapa kata 'gandalf' di dalam teks berikut. (tidak case sensitive)
```
teks = "Centuries later, during the War of the Ring, Gandalf leads Aragorn, Legolas, Gimli, and King Théoden to Isengard, \
        where they reunite with Merry and Pippin. Gandalf retrieves the defeated Saruman's palantír. Pippin later looks  \
        into the seeing-stone and is seen by Sauron. From Pippin's description of his visions, Gandalf surmises that Sauron \
        will attack Gondor's capital Minas Tirith. He rides there to warn Gondor's steward Denethor, taking Pippin with him."

# kode anda
teks = teks.lower() # buat teks menjadi lower dahulu
jawaban_10 = teks.count('gandalf') # hitung jumlah kata gandalf
print(jawaban_10)
```

11. Untuk setiap kata di teks, cetaklah 2 huruf pertamanya!
```
teks = "Centuries later, during the War of the Ring, Gandalf leads Aragorn, Legolas, Gimli, and King Théoden to Isengard"

for kata in teks.split(): # gundakan metode dalam string untuk memisahkan kata-kata berdasarkan spasi
    print(kata[:2])
```

Berikut adalah pertanyaan untuk materi Looping :
Bob dan Kevin sedang bermain sebuah permainan. Di permainan ini mereka menghitung dari 1 sampai 30, namun mereka harus mengucapkan 'Hooray' pada bilangan kelipatan 3 dan mengucapkan 'Yay' pada bilangan kelipatan 5. Jika bilangan tersebut merupakan kelipatan kelipatan 3 dan 5, mereka harus mengucapkan 'Boom'.
Buatlah sebuah program yang mampu membantu mereka dalam bermain permainan tersebut!

11. Pertama buatlah looping untuk mencetak angka 1 sampai 30.
```
for num in range (30):
    num += 1 # isilah dengan loop yang sesuai
    print(num)
```

12. Tambahkan kondisi untuk mencetak "Hooray" jika bilangan merupakan kelipatan 3
```
for i in range(1,31): # isilah dengan loop yang sesuai
    if i % 3 == 0: # berikan kondisi yang sesuai agar dapat mencetak "Hooray" pada bilangan kelipatan 3
        print('Hooray')
    else:
        print(i)
```

13. Tambahkan kondisi untuk mencetak "Yay" jika bilangan merupakan kelipatan 5
```
for i in range (1,31): # isilah dengan loop yang sesuai
    if i % 3 == 0: # berikan kondisi yang sesuai agar dapat mencetak "Hooray" pada bilangan kelipatan 3
        print('Hooray')
    elif i % 5 == 0: # berikan kondisi yang sesuai agar dapat mencetak "Yay" pada bilangan kelipatan 5
        print('Yay')
    else:
        print(i)
```

14. Tambahkan kondisi untuk mencetak "Boom" jika bilangan merupakan kelipatan 3 dan 5
```
for i in range (1,31): # loop
    if i % 3 == 0 and i % 5 == 0: # Kondisi 1
        print('Boom')
    elif i % 5 == 0: # Kondisi 2
        print('Yay')
    elif i % 3 == 0: # Kondisi 3
        print('Hooray')
    else:
        print(i)
```
