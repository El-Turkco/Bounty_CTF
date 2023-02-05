# Bounty_CTF
TRYHACKME Bounty CTF çözümü.

![Nmap Scann](https://user-images.githubusercontent.com/103064152/216838498-e8dd10e1-742c-4b66-a8cb-5b77d5477acc.png)

İlk olarak Nmap  çalıştırıyoruz. Daha sonra FTP açık olduğunu için anonymous giriş varmı kontrol ediyoruz.

![Ftp Login](https://user-images.githubusercontent.com/103064152/216838644-14c81a0d-c2ef-49ac-808f-af43898f75be.png)

Giriş yaptıktan daha sonra içerideki dosyaları get komutu ile alıyoruz.

![Ftp password dosyası](https://user-images.githubusercontent.com/103064152/216838744-9dde10ee-cc47-436b-991b-f4f74228751b.png)

"locks.txt" dosyasının içerisine baktığımızda bu dosyanın password dosyası olduğunu anlıyoruz.

Daha sonra  FTP'den aldığımız diğer dosya'dan kullanıcı adını buluyoruz "lin" 

Hydra araçını kullanarak ssh bruteforce yapıyoruz. 

![hydra kullanımı](https://user-images.githubusercontent.com/103064152/216838995-c26dd8cc-ff9b-435b-a42f-332743f11d15.png)


Password bulduktan sonra SSH giriş yapıyoruz.

![ssh Login](https://user-images.githubusercontent.com/103064152/216839107-c32bb9e4-af52-4e57-a674-8a78f6b4e517.png)

cat user.txt ile userFlag alıyoruz.

![User Flag](https://user-images.githubusercontent.com/103064152/216839231-4846da31-44db-4753-9233-937fea42fe34.png)

Daha sonra "sudo -l" yaparak root yetkilerine bakıyoruz.

![Yetki yüksetme](https://user-images.githubusercontent.com/103064152/216839273-4b11de5c-32ec-412c-b8cd-5087ae464966.png)

"bin/tar" komutunu ile root olmaya çalışıyoruz.

![Root olma](https://user-images.githubusercontent.com/103064152/216839322-1af2c330-6a94-47b9-b0da-9abb4197d082.png)




