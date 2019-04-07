# processchat
Process Communication with Python3

                                                          #ENGLISH#
GOAL:
To learn and monitor two processes communicating over a file and sending signals to each other using Linux signals.

FEATURES OF THE PROGRAM:
Python is coded with version 3.6.7.
Python 3 libraries used “os, signal and time”
Linux is coded on 4.18.0.
Process1 and Process2 can be run as (chmod + x) ./processnumber after being allowed to run. 
In case of error (python3 is not installed under usr / bin) you can enter the directory where the programs are located 
and write python3 processnumber.py.

WORKING LOGIC OF THE PROGRAM:
The process1 waits for the pid number of the process2 after the process1 prints its pid number to the file. 
After Process2 runs, it takes the pid number of process1 to the ı target p variable and puts itself to sleep. 
After entering the pid number of process1 to process1, process1 writes the contents of the yazar message yazar variable 
to the Chat.txt file into the file and goes to sleep by sending the SIGUSR2 signal to process2. The process2 receiving 
the SIGUSR2 signal passes its message into the txt file and goes to sleep by sending SIGUSR1 signal to process1. After 
that, the two processes continue in the form of automatic communication with the SIGUSR1 and SIGUSR2 signals.

                                                          #TÜRKÇE#
AMAÇ:
İki processin Linux sinyallerini kullanarak bir dosya üzerinden haberleşmesini ve birbirlerine sinyal yollamalarını öğrenmek 
ve gözetlemek.

PROGRAMIN ÖZELLİKLERİ:
Python 3.6.7 versiyonu ile kodlanmıştır.
Python 3 kütüphanelerinde “os, signal ve time” kullanılmıştır.
Linux 4.18.0 kerneli üzerinden kodlanmıştır.
Process1 ve Process2’ye çalıştırılabilme izini verildikten sonra (chmod +x) ./processnumarası şeklinde çalıştırılabilir. 
Hata verme durumunda (python3’ün usr/bin altında kurulu olmaması gibi) programların bulunduğu dizine girip python3 
processnumarası.py yazarak ulaşabilirsiniz.

PROGRAMIN ÇALIŞMA MANTIĞI:
process1 kendi pid numarasını dosyaya yazdırdıktan sonra process2’nin pid numarasını kullanıcıdan beklemektedir. 
Process2 çalıştıktan sonra process1’in pid numarasını alıp “target” değişkenine atar ve kendini uykuya alır. process1’e 
process2’nin pid numarası girildikten sonra process1 Chat.txt dosyasına “message” değişkeninin içeriğini dosyaya yazar ve 
process2’ye SIGUSR2 sinyalini yollayarak uykuya geçer. SIGUSR2 sinyalini alan process2 kendi mesajını txt dosyasına yazarak 
process1’e SIGUSR1 sinyalini yollayarak uykuya geçer. Bundan sonrası iki processin otomatize bir şekilde birbirlerine SIGUSR1
ve SIGUSR2 sinyalleri ile haberleşmesi şeklinde devam eder.

Mücahit ÇERİ
