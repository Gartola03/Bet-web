Kideak:
Beñat Burutaran Maiz(Scrum master), Ander Berruezo Aguirre, Garikoitz Artola Obando, Eneko Ballesteros Echeverria

Inplementatutako erabilpen kasuak:
-Create event
-Create question
-Create quote
-Query questions
-Login
-Register

Internalizazioa:
BAI

Arazo nagusiak:
-CreateEventGUI klasean, gertaera berriak sortzean aplikazioan ez ziren ikusten nahiz eta datu-basean sartu.
Konpontzeko gertaera berriaren dataren ordua 00:00ra aldatu dugu UtilDate.trim() metodoarekin.
-CreateQuoteGUI klasean gertaerarik gabeko data bat aukeratzean, exception bat altxatzen zen galderen ComboBox-a
galderak kargatzen saiatzen zelako, hau gertatzen zen gertaeren ComboBox-ean aukeratutako gertaera null zelako.
Baldintza bat jarri dugu galderak gertaera null ez denean bakarrik kargatzeko.
-DataAccess klaseko createQuote() metodoak hasieran arazoak ematen zizkigun. Kuota sartzean, galdera gertaeraren
listatik ezabatzen eta berriro gehitzen saiatzean, datu-baseak ez zigun uzten. Konpontzeko, galdera listatik zuzenean
editatu dugu kuota bere listan sartuz.
-Aurreko errorea konpondu ondoren, beste errore bat sortu genuela konturatu ginen. Kuota sortzeko lehioan, kuota bat
sortzean eta berriro sortzen saiatzean, berriro sartzea uzten zuen aplikazioak nahiz eta berdinak izan.
Hau konpontzeko, QuoteAlreadyExist exception altzatzeko baldintza aldatu genuen, comboBox-ean aukeratutako
galderaren(berriro aukeratu arte eguneratzen ez dena) kuota bektorea konprobatu ordez, zuzenean gertaeraren galdera
bektoreko dagokion posiziotik hartu genuen galdera(datu-basean eguneratuta dagoena). Hau ondo funtzionatzen zuen,
baina geroago metodo askoz sinpleago bat aurkitu genuen hau guztia egiteko. Gerteraren galdera bektoretik galdera
hartu ordez, parametrotik jasotako galderaren zenbakia hartu eta zuzenean find()-ekin bilatzen dugu. Horrela, galderari
zuzenean kuota gehitzen diogu eta dena ondo eguneratzen da bektorerik ukitu gabe.

Erabilitako orduak:
21 ordu

Bideoa:
https://youtu.be/xom6jka3n7I
