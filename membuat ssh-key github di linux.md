1. Masuk ke terminal
2. Pastikan di komputer anda sudah ada direktori ssh, jika tidak ada kita tinggal membuat nya kemudian masuk ke direktori tersebut

    mkdir ~/.ssh    
    cd ~/.ssh 
 
3. Selanjut nya membuat ssh-key nya dengan perintah di bawah ini

        ssh-keygen -t rsa -C "emailgithubkamu@mail.com" -b 4096

Setelah itu akan di minta untuk mengisi id SSH and passphrasenya. Kita bisa menulis id nya, disini saya menulis dengan huruf y. kemudian mengosongkan passphrasenya, setelah itu tekan entar

4. Maka sekarang di direktori ssh ada 2 file dengan nama y dan y.pub. Untuk melihat nya yaitu dengan ketikan perintah ls.
File tanpa ekstensi adalah private key-nya dan file dengan ekstensi .pub adalah public key-nya.

5. Kemudian anda dapat mengambil isi dari public key tadi , lalu paste ke akun github anda.
Untuk melihat isi file dari public key tadi yaitu dengan ketikan perintah

cat y.pub

kemudian select dan salin isi nya dan paste ke kolom ssh di akun github anda.

6. Terakhir kalian bisa mengetes nya di terminal dengan mengetikkan 

ssh -T git@github.com

Jika muncul pesan "You've successfully authenticated, but GitHub does not provide shell access". Maka artinya berhasil di buat dan di tambahkan.
Jika pesannya "permission denied", artinya SSH keynya belum berhasil di tambahkan. 

Kita harus menambahkan nya terlebih dahulu dengan cara mengetikan salah satu perintah di bawah ini

ssh-add ~/.ssh/y
ssh-add ~/.ssh/y.pub

Nah jika sudah harus nya pesan nya seperti You've successfully authenticated". Maka sekarang anda bisa menggunakan ssh.
