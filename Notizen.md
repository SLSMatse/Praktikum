## Server verbindung
IP-Adresse Server: 142.132.180.233
ssh-verbinden = mattis@142.132.180.233

## Allgemeine befehle
ping-befehl = Checkt ob Computer verbindung mit Server hat.
password-change = passwd
sudo (Befehl) = Führt befehl mit Admin rechten aus, d.h. dass User ohne Admin rechte diese Datei nicht löschen/benutzen können.

sort = Sortier ein Text nach dem ABC.

## Mark-down
Markdown ist eine Auszeichnungssprache zur einfachen Textformatierung.
Markdown wird benutzt um Dateien zu formatieren und Texte zu verfassen.

## Verzeichnis anlegen/Löschen
### Anlegen
mkdir = Verzeichnis erstellen
cd (Name) = Zu anderem Verzeichnis navigieren
pwd = Zeigt an in welchem Verzeichnis man sich befindet.
ls = Schauen was in einem Verzeichnis sich befindet.
### Löschen
rm -r = Befehl um Verzeichnix inklusive alle darin enthaltenen dateien zu löschen.

## Datei kopieren/löschen/Verschieben/Erstellen/Anzeigen/Öffnen
#### Kopieren
cp = Kopier-Befehl
cp-Quelle-Ziel
Statt [Quelle(n)] gebe Dateiname oder Verzeichnis ein, bsp: "datei.txt".  
Für das [Ziel]gebe das **Zielverzeichnis** ein, in das die entsprechende Datei kopiert werden soll, beispielsweise "home/username/Dokumente".  

### Löschen
rm = Löschen-Befehl

rm-Quelle
Statt [Quelle(n)] gebe Dateinamen oder Verzeichnis ein, bsp: "datei.txt". 

### Erstellen
touch-befehl = 
Erstellt dateien oder um dateien zugriff und änderungs berechtigungen zu ändern.

### Verschieben
mv = Datei verschieben
mv test.txt ~/TestOrdner

### Anzeigen
ls = Schauen was in einem Verzeichnis sich befindet.
ls -la = Zeigt alle Versteckten dateien ink. Berechtigungen und Änderungs daten an, im Verzeichnis an, auch alle dateien auf die der User kein Zugriff drauf hat.
ls -la /etc = Zeigt alle dateien an mit dessen Berechtigungen, auch dessen neben dateien.
ls /etc = Gibt alle dateien aus.

### Öffnen
cat (quelle) = Öffnet eine Datei, sodass man ihren inhalt anschauen kann.

## User erstellen/Löschen/Ändern/Wechseln/Gruppe
### Erstellen
useradd = Erstellt einen neuen User. Der Befehl useradd muss mit dem Admin befehl sudo ausgeführt werden.

useradd Test123 = Erstellt einen neuen User mit dem namen Test 123
sudo useradd Test123

### Löschen
userdel Test123 = Löscht den User mit dem Namen Test123.

### Ändern
passwd Test123 = Ändert das Passwort von dem User Test123.
who = Zeigt an welche User auf den Server connected sind und datum,Uhrzeit sowie IP-Adresse vom User.

### Wechseln
su = Befehl um zwischen Usern zu wechseln.
su Mogwai = Wechselt den User auf den User Mogwai.

### Gruppe
usermod -aG = Fügt einen User zu der gewünschten gruppe hinzu.

sudo usermod -aG sudo Mogwai

chmod +rwx test123.txt = Gibt allen Usern die berechtigung die datei test123.txt zu lesen, schreiben und auszuführen.

chmod -rwx test123.txt = Nimmt allen Usern die berechtigung die datei test123.txt zu lesen, schreiben und auszuführen.

chmod o+rwx test123.txt = Gibt dem jetzigen User die Berechtigung die Datei test123.txt zu verändern zu lesen und auszuführen.

## Nano

### Verändern
nano (Datei-Name) = Befehl um datei zu öffnen und verändern.

## Herunterladen
wget (URL) = Lädt die Datei von der URL runter und zieht sie in den Geöffneten Ordner.
wget https://mogwailabs.de/logo.svg = Lädt das Mogwai labs logo herunter.#

wget -o Test123.svg https://mogwailabs.de/logo.svg = Lädt das Mogwai-labs logo herunter und packt es in den geöffneten ordner wo es Test123.svg benannt wird.

## Tar-Dateien
Dateien in ein Tar-Archiv packen = tar cfv Test.tar datei1 datei2 datei3 ...
Dateien in ein Komprimiertes Tar-Archiv packen = tar cfzv Test.tar datei1 datei2 datei 3 ...
Tar-Archiv entpacken = tar xfv Test.tar
Inhalt eines Tar-Archivs anzeigen = tar tfv Test.tar

## Tgz-Dateien
Dateien in ein Tar-Archiv packen = tar cfvz Test.tar.gz datei1 datei2 datei3 ...
Dateien in ein Komprimiertes Tar-Archiv packen = tar cfzv Test.tar.gz datei1 datei2 datei 3 ...
Tar-Archiv entpacken = tar xfv Test.tar.gz

### Grep
grep Wolf test123.txt = Der grep befehl sucht in diesem fall aus der datei test123.txt alle zeilen raus die den Text WOLF enthalten.

### Cut
cut -d "=" = filtert jedes = aus der datei heraus.

### Uniq
uniq -c "test123.txt" = Filter alle doppelte namen im text test123.txt heraus und schreibt die anzahl dazu.