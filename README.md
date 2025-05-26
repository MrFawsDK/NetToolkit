# Netværksværktøj (Network Tool)

Et alsidigt kommandolinjeværktøj til netværksdiagnostik og -sikkerhedsanalyse med en farverig brugervenlig grænseflade.


## Funktioner

Netværksværktøjet indeholder seks hovedfunktioner:

1. **DNS-opslag**: Find IP-adresserne der er knyttet til et domænenavn
2. **Ping Test**: Mål svartiden til et domæne eller en IP-adresse
3. **Geolokation**: Find den fysiske placering af en IP-adresse
4. **Port Scanning**: Scan efter åbne porte på et mål
5. **WHOIS Lookup**: Få registreringsoplysninger om et domæne
6. **Subdomæne Scanning**: Find mulige subdomæner til et givent domæne

## Installation

### Forudsætninger

- Python 3.6 eller nyere
- Internetforbindelse (for geolokation og WHOIS-opslag)

### Trin-for-trin installation

1. Clone eller download dette repository:
   ```bash
   git clone https://github.com/username/netvaerkvaerktoej.git
   cd netvaerkvaerktoej
   ```

2. Installer de nødvendige Python-pakker:
   ```bash
   python -m pip install requests ping3 python-whois colorama
   ```

3. Kør programmet:
   ```bash
   python main.py
   ```

## Detaljeret Funktionsbeskrivelse

### 1. DNS-opslag
Laver et DNS-opslag for at konvertere et domænenavn til en IP-adresse og viser yderligere DNS-information.

### 2. Ping Test
Sender ICMP-anmodninger til et mål for at måle svartiden og kontrollere om målet er online. Bruger `ping3`-biblioteket hvis installeret, ellers falder tilbage til systemets indbyggede ping-kommando.

### 3. Geolokation
Finder den fysiske placering af en IP-adresse, inklusiv land, by, region, ISP og koordinater. Bruger den gratis ip-api.com tjeneste.

### 4. Port Scanning
Scanner efter åbne porte på et mål ved hjælp af multithreading for hurtig scanning. Genkender almindelige tjenester og giver brugeren mulighed for at scanne kun almindelige porte eller alle velkendte porte (1-1024).

### 5. WHOIS Lookup
Henter registrerings- og ejeroplysninger for et domæne, herunder registreringsdato, udløbsdato og navneservere. Kræver `python-whois`-pakken.

### 6. Subdomæne Scanning
Scanner efter subdomæner til et givent domæne ud fra en ordliste. Giver mulighed for at:
- Bruge den indbyggede ordliste
- Indlæse en brugerdefineret ordliste fra en fil
- Tilføje yderligere subdomæner manuelt

## Brugervejledning

1. Start værktøjet med `python main.py`
2. Vælg en funktion fra hovedmenuen (1-6)
3. Indtast et domæne eller en IP-adresse, når du bliver bedt om det
4. Følg eventuelle yderligere instruktioner på skærmen
5. Resultaterne vises i en farvekodet boks

## Bemærkninger

- **Performance**: Port scanning og subdomæne scanning kan tage længere tid afhængigt af målserver og det antal porte/subdomæner, der skal scannes.
- **Juridisk bemærkning**: Brug kun dette værktøj på systemer, du har tilladelse til at analysere. Uautoriseret scanning kan være ulovlig.
- **Fejlfinding**: Hvis du oplever problemer med WHOIS eller ping, sørg for at de valgfrie pakker er korrekt installeret.

## Valgfrie Pakker

- `ping3`: For avanceret ping-funktionalitet
- `python-whois`: For WHOIS-opslag
- `colorama`: For farverig terminaloutput

## Licens

Dette projekt er udgivet under MIT-licensen - se LICENSE filen for detaljer.

## Forfatter

Fawsdev.dk

## Anerkendelser

- ip-api.com for geolokationstjenesten
- python-whois for WHOIS opslag
- colorama for farvefuld terminaloutput
