man iptables (pokazuje dokumentacje dla dowolnego polecenia)

#iptables -F (wyłańczamy wpisy)

#iptables -L (pokazuje wpisy)


Pobieramy skrypt w linuxie na pow�oce systemowej (ang. shell

wget --no-check-certificate http://keca13.vot.pl/algo/skrypt/sciagnij.

wget --no-check-certificate https://raw.githubusercontent.com/keca13/keca13_linux/master/sciagnij.txt

Odpalamy skrypt

sh sciagnij.txt


Lokalizacja skryptu

/etc/init.d/skrypt

sprawdzamy dzia�anie skryptu np. n

http://www.traceroute.org/

wyłaczamy wpisy IPTABLES na: /etc/init.d/skrypt

=====================
man awk

#$2 druga kolumna #',' seoarator kolumny

awk -F ',' '{print $2}' plik.txt

=======================
cat plik.txt | grep 'szukany text'

grep '^napoczatkuwiersza' plik.

grep 'nakoncu wiersza$' plik.txt

history | grep iptables


===============

Usuwamy białe znaki np.^M

#-i bak    tworzy plik o takiej samej nazwie z rozszeżeniem ca.pem.bak

sed -i.bak 's/^M//g' ca.pem

sed -i.bak 's/,//g' contact.txt

^M=press(Ctrl-V Ctrl-M

vi ca.pem


--------------
vi file
i # tryb edycji
esc # wyjscie z trybu

:x # wyjscie z zapisem
:q! # bez zapisu

Podstawowe komendy:
Wprowadzanie tekstu: a,i,A,i
Usuwanie tekstu: x (DEL), X (BACKSPACE)
Zapisywanie: ZZ, :w nowanazwa, :w
Wyjscie bez zapisywania :q! Dzialanie guzikow a oraz i:
Przesuwanie tekstu: l,k,j,h
Wstawianie linii: o
Kopiuj inie: yy
Wklej: p
Kasowanie linii: dd
Kasowanie do konca linii: D
Przesuwanie tekstu: $, 0, ^F, ^B, w, b,[[,]]
Wyszukiwanie: /
==================================
# Za pomocą polecenia w możemy otrzymać wiele ciekawych informacji, takich jak np. kto jest zalogowany, jakich procesów jaki użytkownik używa,
# zawiera się tu także polecenie uptime. Użycie polecenia jest następujące. 
w
==================================
# kopiowanie z serwera na serwer

#Kopiowanie pliku ze zdalnej lokalizacji na lokalny dysk
$ scp uzytkownik@serwer.pl:/scieżka/plik_serwer plik_lokalny
#Kopiowanie pliku z dysku lokalnego do zdalnej lokalizacji
$ scp plik_lokalny uzytkownik@serwer.pl:/sciezka/plik_serwer


scp debian-10.3.0-amd64-DVD-1.iso root@X.X.X.X:/var/lib/vz/template/iso/

#Kopiowanie pliku ze zdalnej lokalizacji na lokalny dysk
scp root@10.X.0.X:/home/sample.txt /home/sample.txt


=======================
PYTHON3.8
# https://linuxize.com/post/how-to-install-python-3-8-on-debian-10/

sudo apt update | sudo apt-get update | sudo aptitude update
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libsqlite3-dev libreadline-dev libffi-dev curl libbz2-dev
curl -O https://www.python.org/ftp/python/3.8.2/Python-3.8.2.tar.xz
tar -xf Python-3.8.2.tar.xz
cd Python-3.8.2
./configure --enable-optimizations
nproc
make -j 4
sudo make altinstall #Do not use the standard make install as it will overwrite the default system python3 binary.
python3.8 --version

# we’ll create a new Python 3.8 project called my_app inside the user home directory.
mkdir ~/my_app && cd ~/my_app

# Creating a Virtual Environment

python3.8 -m venv my_app_venv
source my_app_venv/bin/activate # From inside the project root run the following command to create a virtual environment named my_app_venv:
python -v
deactivate

=========================
#cat /etc/network/interfaces
or
#cat /etc/dhcpcd.conf
or 
# cat /etc/wpa_supplicant/wpa_supplicant.conf
=============================
#echo "Hello world" > drzewko.txt
#echo "Hello world" >> drzewko.txt
operator > nadpisuje cały plik tym, co zostanie przekazane. 
Natomiast operator >> dopisuje przekazane informacje na końcu pliku!

=========================
MONTOWNIE DYSKU

df
df -aTh
df -Th

Disk /dev/sda
Device /dev/sda1
#mkdir /mnt/backups
fdisk -l
#sudo mount /dev/sda2 /mnt/
#sudo umount /dev/sda2

# in this path is auto default, if after default is problem you just commant disk
/etc/fstab

========================
"uptime": "uptime | awk '{print $3,$4}'"
 "cat": "cat /home/pi/test.txt",
	"grep": "grep -i A /home/pi/test.txt",
	"grep2": "grep -i A$ /home/pi/test.txt",
	"grep3": "grep -i ^A /home/pi/test.txt",
	"hostname": "hostname",
	"sed -i -e '1,4s/22/999/' /home/pi/test.txt"


=====================================

LOGI SYSTEMOWE

cat /var/log/syslog
tail -f /var/log/syslog

tail -f /var/log/auth.log

PROCESY

top


ZALOGOWANI

w
======================

Podstawowe komendy i polecenia w Linux
I. Polecenia związane z użytkownikami, grupami, loginami i zamykaniem systemu
o shutdown(zamykamy Linuxa)
o adduser (dodajemy nowego użytkownika)
o newgrp (dodajemy nową grupę)
o passwd (zmieniamy hasła)
o logout (wylogowanie się)
o who (sprawdzamy kto jest aktualnie zalogowany)
o users (j/w)
o w (j/w)
o whoami (sprawdzamy kim jesteśmy)
o mesg (zezwolenie na przyjmowania komunikatów)
o write (wysłanie wiadomości do danego użytkownika)
o wall (j/w tylko do wszystkich użytkowników)
o rwall (j/w tylko do wszystkich w sieci)
o ruser (wyświetla użytkowników pracujących w systemie)
o talk (możliwość interaktywnej rozmowy)
o finger(szczegółowe informacje o użytkownikach)
o su (zmieniamy się w innego użytkownika)
o chmod (zmieniamy parametry pliku)
o chown (zmieniamy właściciela pliku)
o chgrp (zmieniamy jaka grupa jest właścicielem pliku)
II. Polecenia związane z plikami i katalogami
o Polecenia związane z katalogami
 ls (pokazuje nam zawartość katalogu)
 dir (okrojona wersja ls, pochodząca z msdos'a)
 pwd (pokazuje nam katalog w którym się znajdujemy)
 cd (zmieniamy katalog)
 rmdir (usuwamy katalog)
 mkdir (nowy katalog)
o Polecenia związane z plikami
 cat (edytowanie tekstu)
 rm (usuwamy plik(i))
o Polecenia związane z kopiowaniem i przenoszeniem, plików i katalogów
 mv (przenosimy plik lub zmieniamy jego nazwę)
 cp (kopiujemy plik)
 mvdir (przenosimy katalog lub zmieniamy jego nazwę)
III. Polecenia związane z procesami
o ps (pokazuje nam jakie procesy są aktualnie wykonywane)
o kill ("zabijamy" procesy)
IV. Polecenia związane z pomocą
o help (wyświetla nam wszystkie polecenia w Linuxie)
o man (pokazuje nam pomoc do programu)
V. Polecenia związane z kompresją i archiwilizacją
o gzip(kompresuje nam archiwum *.gz)
o tar (archiwizuje nam archiwum *.tar)
 

==========================================================

scp -P port vi-editor.rd root@192.168.X.X:/home/pi
scp -P port root@192.168.x.x:/home/pi/plik_serwera.txt plik_lokalny.txt
scp -P port plik_lokalny.rd root@192.168.X.X:/home/pi


iptables -F
#sudo service nazwa_uslugi start
#sudo service nazwa_uslugi stop
#sudo service nazwa_uslugi restart
A jak byscie chcieli wylaczyc skrypt to wystarczy skorzystac z polecenia:

#sudo update-rc.d nazwa_uslugi remove

#/etc/rc.local
powyzej,jest to plik przetwarzany przy kazdym starcie systemu 
– mo¿emy tu dodaæ polecenie lub œcie¿kê do skryptu 
który ma siê wykonaæ podczas startu systemu.
Zasada jest banalna – po prostu przed linijk¹ „exit 0” dodajemy np.:

echo "System zostal uruchomiony"
Lub:

/sciezka/do/skryptu
np.:  /etc/init.d/skrypt
