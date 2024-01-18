Germans Veidemans 3.grupa
231RDB234
# ss.com sludinājumu meklēšana

Kadreiz cilvēks nolēma izveidot automašīnu nomas uzņēmumu. Viņš sapulcināja komandu, atrada biroja telpas. Komandā viņi nolēma, ka, lai sāktu, viņiem jāiegādājas lietota mašīna ar dažādu cenu diapazonu, dažādām klasēm, ar dažādu jaudu, lai klients varētu izvēlēties viņam piemērotāko variantu. Vienīgā vietne, kur var iegādāties lietotu automašīnu, ir ss.com. bet manuāli meklēt ļoti ilgi, jo viņi vēlas sākt pēc iespējas ātrāk. Viņiem ir fails ar katras auto parametriem. Jums jāizveido tabula, kurā tiks apkopotas visas iespējamās iespējas katram parametram.

## Programmas uzdevums

 Programma izpilda sekojošas darbības:
 1. Nolasa datus no faila options.csv. Failā atrodas tādi parametri: Cena, Gads, Dzinēja tilpums, Dzinējs, Ātruma kārba, Virsmas tips, Krāsa. Krāsas vietā varbūt "-" zīme, kas nozīme jebkura krāsa, jo krāsa nav tik svarīga. Dzinēja tilpuma vietā var ierakstīt gan vienu ciparu, gan divus ciparus caur "-", gan vienkārši "-", jo vēl ir elektriskie auto.
 2. Ievietot options.csv datus ss.com vietnē.
 3. Atrast visus iespējamus sludinājumus pēc parametriem.
 4. Ievietot sludīnajumu informāciju tabulā result.xlsx, kur būs tik lapas, cik ir options.csv parametru. Tabulā ir ierakstīts markas nosaukums un modelis, gads, dzinēja tilpums, nobraukums, cena un saite uz sludinājumu.

## Python bibliotēkas

Programmā tiek izmantoti selenium, openpyxl, pandas un time bibliotēkas.
Selenium izmantošana, dod iespēju nodarboties ar ss.com vietni.
Openpyxl ir izmantota, lai pierakstītu rezultātus excel failā result.xlsx
Izmantojot bibliotēku pandas, var nolasīt datus no faila options.csv
Un time dod iespēju apstradāt visus sludinājumu no ss.com vietnes un pierakstīt to result.xlsx failā.

## Programmatūras izmantošanas metodes

Programmā ir redzami divas funkcijas, Find_information un Fill_Cells.
Fill_Cells funkcija ievieto datus ss.com šūnās, lai atrastu sludinājumus.
Find_information funkcijas meklē informāciju par katru sludinājumu un pieraksta info excel tabulā.
Kā arī tiek izmantoti cikli.
