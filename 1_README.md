# PPP

1.	Importo la tabella dati
2.	Faccio la distinct ridotta al minimo (tolgo country, valori numerici, food, sostanze)
3.	Faccio proc contents per vedere quali cataloghi importare)
4.	Scarico “reporting data  on pesticide residues” EFSA
5.	Prendo la tabella della SSD2 e la uso su file excel per associare i cataloghi ai data elements (NB errori: SRCTYP e’ in realta’ PRGTYP, MDSTAT e’ probabilmente MDACC, verificare), aggiungere MATRIX per prodcode, PARAM per PARAMCODE, COUNTRY per vari
6.	Importare i cataloghi (probabilmente andranno importati con il wizard)
7.	Scrivere la macro per I formati
8.	Creare I formati
9.	Applicare I formati alla fact table
10.	Creare report base come richiesto…


Nota bene:
Per fare il conto dei campioni devo fare prima una preparatory table (summary) con proc sql; due possibilita’:
1.	Seleziono distinct labsampcode e le variabili che mi servono
2.	Produco gia’ le frequenze nella summary table con grouping corrispondente (+ rischioso perche’ se poi cambio livello di aggregazione puo’ sballare tutto, ma soluzione che velocizza la proc report seguente)
