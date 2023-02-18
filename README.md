# FIIT-STU-project

Napíšte program, ktorý bude pracovať so záznamami zapísanými v súbore predaj.txt obsahujúci záznamy o predaji áut. Program bude vykonávať príkazy načítané zo štandardného vstupu. Každý príkaz bude predstavovať malé písmeno nasledované koncom riadku a to:
 v – po aktivovaní program otvorí súbor a vypíše jednotlivé záznamy zo súboru na obrazovku. Jednotlivé záznamy budú oddelené prázdnym riadkom, jednotlivé položky záznamu budú pomenované a každá bude umiestnená v samostatnom riadku. Záznam o predaji áut bude vyzerať takto:
meno priezvisko:(medzera) meno predávajúceho, max. 50znakový reťazec, ktorý obsahuje písmená a medzery
SPZ: (medzera) štátna poznávacia značka, sedemmiestny znakový reťazec tvaru AACCCBB, kde AA sú dva abecedné znaky reprezentujúce skratku okresu, CCC sú tri číselné znaky a BB sú dva abecedné znaky (napr. BA354SC)
typ auta:(medzera) booleovská hodnota (1 pre nové auto, 0 pre ojazdené auto)
cena: (medzera) reálne číslo z intervalu <100.00, 600000.00>, vždy s dvoma desatinnými miestami
datum: (medzera) dátum nástupu do zamestnania, osemmiestne celé číslo v tvare rrrrmmdd 20180330 (30.3.2018)
(prázdny riadok)
Súbor bude obsahovať iba hodnoty, nie typy (názvy) položiek..
V prípade ak sa súbor nepodarí otvoriť vypíše správu Neotvoreny subor
Správa je nasledovaná znakom konca riadku.
 o – po aktivovaní program načíta aktuálny dátum vo formáte rrrrmmdd. Následne vypíše zoznam odmien pre zamestnancov, ktorým sa udeľuje odmena (pričom znovu načítava vstupný súbor). Zoznam bude pozostávať z mena a priezviska, SPZ a odmeny pre zamestnanca, ktorý predal auto s danou SPZ v jednom riadku. Jednotlivé položky v riadku sú oddelené vždy jednou medzerou. Odmena sa udeľuje zamestnancom, ktorí pracujú aspoň jeden rok. Výška odmeny sa určuje podľa typu predaného auta takto: 1.5% z ceny nového, alebo 2.5% z ceny ojazdeného auta. Odmenu vypisujte na dve desatinné miesta (výpis - podľa poradia v súbore, aj viackrát pre jedného zamestnanca ak predal viac áut po jednom roku v tomto zamestnaní). Ak súbor nie je otvorený (t.j. ešte nebol vykonaný príkaz v), alebo ak neexistuje žiaden zamestnanec pracujúci aspoň rok, ktorý predal auto, táto voľba negeneruje žiaden výstup.

 n – po aktivovaní spočíta počet záznamov v súbore, dynamicky vytvorí pole znakov a položky typu SPZ zo súboru zapíše do poľa v takom poradí, v akom sú v súbore. Ak už bolo pole predtým vytvorené, je najprv dealokované a potom sa vytvorí nové. Pri tejto voľbe program negeneruje žiaden výstup. Ak súbor nie je otvorený (t.j. ešte nebol vykonaný príkaz v), táto voľba nič nezmení.
 s – vypíše položky typu SPZ z dynamicky alokovaného poľa na obrazovku v tvare: AA CCC BB
BA 353 AB
SC 128 BD
BL 585 LB
BA 854 BA
Ak pole nie je vytvorené, vypíše správu Pole nie je vytvorene Správa je nasledovaná znakom konca riadku.
 p – vypíše skratku zo SPZ určujúcu okres v prípade ak SPZ je palyndróm. Napríklad, ak pole obsahuje SPZ BA353AB, SC128BD, BL585LB, BA854BA na výstupe bude:
BA
BL
Ak pole nie je vytvorené, vypíše správu Pole nie je vytvorene Správa je nasledovaná koncom riadku.
 z – zistí a vypíše z ktorého okresu sa predalo najviac áut. Za skratkou okresu nasleduje medzera a počet predaných áut. Napríklad, ak pole obsahuje SPZ BA353AB, SC128BD, BL585LB, BA854BA na výstupe bude:
BA 2
Ak existuje viac skratiek pre jeden okres napr. BA a BL počítajú sa ako dve rôzne skratky. Ak pole nie je vytvorené, táto voľba nič nezmení.
k – ukončí program. Pri tejto voľbe program negeneruje žiaden výstup.
Predpokladajte, že vstup je zadaný správne a preto ho nie je potrebné ošetrovať. Príkazy sa načítavajú zo štandardného vstupu a výstup sa má vypísať na štandardný výstup.
