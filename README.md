Ovo je React funkcionalna komponenta koja prikazuje popis korisnika i omogućuje pretraživanje korisnika po gradu i sortiranje po imenu. 

Također, omogućuje prikazivanje samo određenog broja korisnika po stranici i navigaciju između stranica.

Prvo, importujemo React, useState i useEffect hookove iz Reacta i axios biblioteku za obavljanje HTTP zahtjeva. Također, importujemo CSS datoteku.

Zatim definišemo tip korisnika pomoću interface-a koje ima id, ime, adresu, telefon i naziv tvrtke.

Nakon toga definišemo funkciju komponentu App koja koristi nekoliko useState hookova za pohranjivanje stanja. 

Prvi useState hook pohranjuje popis korisnika, drugi hook pohranjuje termin za pretraživanje korisnika. 

Treći hook pohranjuje trenutnu stranicu koju korisnik pregledava, a četvrti hook pohranjuje smjer sortiranja. (ASC DESC)

Zatim koristimo useEffect hook koji se poziva samo jednom prilikom prvog renderiranja komponente. 

Ovaj hook se koristi za dohvatanje popisa korisnika pomoću HTTP GET zahtjeva na web API putanju 'https://jsonplaceholder.typicode.com/users'. 

Rezultati se pohranjuju u stanje korisnika. Nakon toga definišemo nekoliko pomoćnih funkcija. 

handleSearchTermChange obrađuje promjene u pretraživanju korisnika i postavlja trenutnu stranicu na prvu. 

handleSortDirectionChange preokreće smjer sortiranja. 

sortedUsers i filteredUsers pomoću Array.sort() i Array.filter() sortiraju i filtriraju korisnike prema abecedi i pretraživanju grada. 

Konačno, handlePageChange ažurira trenutnu stranicu kada korisnik klikne dugme za navigaciju.

Na kraju funkcije App renderira JSX koji prikazuje polje za pretraživanje, tablicu s popisom korisnika, dugme za navigaciju i koristi pohranjene vrijednosti iz useState hookova i pomoćnih funkcija za dinamičko prikazivanje podataka. 

Sortirani korisnici se prikazuju u tablici s imenom, adresom, telefonom i nazivom tvrtke. 

Također, strelica prema gore ili dole se prikazuje ovisno o trenutnom smjeru sortiranja. 

Dugme za navigaciju generišemo pomoću Array.from() i map() metoda i dodajemo CSS klasu "active" na trenutnu stranicu.

Ovo je jednostavan primjer funkcionalne React komponente koja koristi useState i useEffect hookove, HTTP GET zahtjev, sortiranje i filtriranje polja i navigaciju stranica kako bi prikazala popis korisnika u tablici.
